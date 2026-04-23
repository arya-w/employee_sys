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

    /* ---------------- DEBUG STAGE ---------------- */
    stage('Debug Docker Credentials') {
      steps {
        withCredentials([usernamePassword(
            credentialsId: 'dkr',
            usernameVariable: 'U',
            passwordVariable: 'P'
        )]) {
          bat '''
            echo Checking Docker credentials...
            echo Username = %U%
            echo Password length check:
            echo %P% | findstr /R "."
          '''
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
            credentialsId: 'dkr',
            usernameVariable: 'DOCKER_USERNAME',
            passwordVariable: 'DOCKER_PASSWORD'
        )]) {

          bat '''
            echo Logging into Docker Hub...

            echo %DOCKER_PASSWORD%>pass.txt
            docker login -u %DOCKER_USERNAME% --password-stdin < pass.txt
            if %errorlevel% neq 0 exit /b %errorlevel%
            del pass.txt

            echo Login successful
            docker push %DOCKER_IMAGE%:%DOCKER_TAG%
            docker push %DOCKER_IMAGE%:latest
            docker logout
          '''
        }
      }
    }

    stage('Deploy') {
      steps {
        bat '''
          echo Cleaning up old container...
            docker stop springboot-app 2>nul || exit 0
            docker rm springboot-app 2>nul || exit 0
            
            echo Starting container...
            docker run -d -p 8085:8085 --name springboot-app %DOCKER_IMAGE%:latest
            
            echo Container started successfully!
            exit 0
        '''
      }
    }
  }

  post {
    success {
      echo 'Pipeline completed successfully!'
    }
    failure {
      echo 'Pipeline failed! Check logs above.'
    }
  }
}