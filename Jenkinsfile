pipeline {
  agent any
  
  tools {
    maven 'Maven'  
  }
  
  environment {
    DOCKER_IMAGE = 'aryaw7/employee-sys'
    DOCKER_TAG = "${BUILD_NUMBER}"
  }

  stages {
    stage('Checkout') {
      steps {
        git branch: 'main',
            url: 'https://github.com/arya-w/employee_sys.git',
            credentialsId: 'git'
      }
    }

    stage('Build & Test') {
      steps {
        bat '''
          echo Building with Maven...
          mvn --version
          mvn clean package
          mvn test
        '''
      }
      post {
        always {
          junit allowEmptyResults: true, testResults: '**/target/surefire-reports/*.xml'
        }
      }
    }

    stage('Docker Build') {
      steps {
        bat "docker build -t %DOCKER_IMAGE%:%DOCKER_TAG% ."
        bat "docker tag %DOCKER_IMAGE%:%DOCKER_TAG% %DOCKER_IMAGE%:latest"
      }
    }

    stage('Docker Push') {
      steps {
        withCredentials([usernamePassword(
            credentialsId: 'Docker',
            usernameVariable: 'DOCKER_USERNAME',
            passwordVariable: 'DOCKER_PASSWORD'
        )]) {
          bat '''
                        echo %DOCKER_PASSWORD% | docker login -u %DOCKER_USERNAME% --password-stdin
                        if %errorlevel% neq 0 exit /b %errorlevel%
                        echo Successfully logged in to Docker Hub
                        docker push %DOCKER_IMAGE%:%DOCKER_TAG%
                        docker push %DOCKER_IMAGE%:latest
                        docker logout
                    '''
        }
      }
    }

    stage('Deploy') {
      steps {
        bat """
          docker stop springboot-app || exit 0
          docker rm springboot-app || exit 0
          docker run -d -p 9090:8085 --name springboot-app %DOCKER_IMAGE%:latest
        """
      }
    }
  }

  post {
    success { 
      echo 'Pipeline completed successfully!' 
    }
    failure { 
      echo 'Pipeline failed! Check the logs above.'
    }
  }
}