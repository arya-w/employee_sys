docker image created : 
<img width="1366" height="768" alt="Screenshot (2)" src="https://github.com/user-attachments/assets/6323745a-7c9e-46c0-a000-c465e2c739e6" />

container docker desktop :
<img width="1366" height="768" alt="Screenshot (7)" src="https://github.com/user-attachments/assets/a139e39f-3cd5-4ee1-ac74-ad6b10d41f3b" />

successful build , .jar file created : 
<img width="1366" height="768" alt="Screenshot (8)" src="https://github.com/user-attachments/assets/aa74b69f-4477-4ba8-9e27-309608c17f80" />

postman tests :
<img width="1366" height="768" alt="Screenshot (14)" src="https://github.com/user-attachments/assets/6018fadf-32f5-44f2-b8ae-be8115c59272" />
<img width="1366" height="768" alt="Screenshot (13)" src="https://github.com/user-attachments/assets/30770271-3142-4ff8-abb4-3414e0a56654" />
<img width="1366" height="768" alt="Screenshot (12)" src="https://github.com/user-attachments/assets/a65e9b8f-aaf4-4411-828d-09c00a959410" />
<img width="1366" height="768" alt="Screenshot (11)" src="https://github.com/user-attachments/assets/abab59be-930a-4c5e-a0da-9c441690842f" />
<img width="1366" height="768" alt="Screenshot (10)" src="https://github.com/user-attachments/assets/de3704e7-2962-40f9-9d05-6473d500cca4" />

Jenkins console LOGS :

[PIPELOGS.txt](https://github.com/user-attachments/files/27008746/PIPELOGS.txt)
Started by user unknown or anonymous
Obtained Jenkinsfile from git https://github.com/arya-w/employee_sys.git
[Pipeline] Start of Pipeline
[Pipeline] node
Running on Jenkins in C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Checkout SCM)
[Pipeline] checkout
The recommended git tool is: NONE
using credential git
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe rev-parse --resolve-git-dir C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe\.git # timeout=10
Fetching changes from the remote Git repository
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe config remote.origin.url https://github.com/arya-w/employee_sys.git # timeout=10
Fetching upstream changes from https://github.com/arya-w/employee_sys.git
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe --version # timeout=10
 > git --version # 'git version 2.54.0.windows.1'
using GIT_ASKPASS to set credentials 
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe fetch --tags --force --progress -- https://github.com/arya-w/employee_sys.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe rev-parse "refs/remotes/origin/main^{commit}" # timeout=10
Checking out Revision 73b978b70d9d6b7c8c5841b802449933cc545826 (refs/remotes/origin/main)
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe config core.sparsecheckout # timeout=10
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe checkout -f 73b978b70d9d6b7c8c5841b802449933cc545826 # timeout=10
Commit message: "update"
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe rev-list --no-walk 07c41b1f7c9a60d96be1cb6774b558d6e6a9aa87 # timeout=10
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] withEnv
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Tool Install)
[Pipeline] tool
[Pipeline] envVarsForTool
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Checkout)
[Pipeline] tool
[Pipeline] envVarsForTool
[Pipeline] withEnv
[Pipeline] {
[Pipeline] git
The recommended git tool is: NONE
using credential git
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe rev-parse --resolve-git-dir C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe\.git # timeout=10
Fetching changes from the remote Git repository
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe config remote.origin.url https://github.com/arya-w/employee_sys.git # timeout=10
Fetching upstream changes from https://github.com/arya-w/employee_sys.git
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe --version # timeout=10
 > git --version # 'git version 2.54.0.windows.1'
using GIT_ASKPASS to set credentials 
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe fetch --tags --force --progress -- https://github.com/arya-w/employee_sys.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe rev-parse "refs/remotes/origin/main^{commit}" # timeout=10
Checking out Revision 73b978b70d9d6b7c8c5841b802449933cc545826 (refs/remotes/origin/main)
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe config core.sparsecheckout # timeout=10
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe checkout -f 73b978b70d9d6b7c8c5841b802449933cc545826 # timeout=10
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe branch -a -v --no-abbrev # timeout=10
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe branch -D main # timeout=10
 > C:\Users\arya.wadikhaye\AppData\Local\Programs\Git\mingw64\bin\git.exe checkout -b main 73b978b70d9d6b7c8c5841b802449933cc545826 # timeout=10
Commit message: "update"
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Build & Test)
[Pipeline] tool
[Pipeline] envVarsForTool
[Pipeline] withEnv
[Pipeline] {
[Pipeline] bat

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>echo Building with Maven... 
Building with Maven...

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>mvn --version 
Apache Maven 3.9.15 (98b2cdbfdb5f1ac8781f537ea9acccaed7922349)
Maven home: C:\ProgramData\Jenkins\.jenkins\tools\hudson.tasks.Maven_MavenInstallation\Maven
Java version: 17.0.12, vendor: Oracle Corporation, runtime: C:\Program Files\Java\jdk-17
Default locale: en_US, platform encoding: Cp1252
OS name: "windows 11", version: "10.0", arch: "amd64", family: "windows"
Post stage
[Pipeline] junit
Recording test results
No test report files were found. Configuration error?
None of the test reports contained any result
[Checks API] No suitable checks publisher found.
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Debug Docker Credentials)
[Pipeline] tool
[Pipeline] envVarsForTool
[Pipeline] withEnv
[Pipeline] {
[Pipeline] withCredentials
Masking supported pattern matches of %P%
[Pipeline] {
[Pipeline] bat

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>echo Checking Docker credentials... 
Checking Docker credentials...

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>echo Username = aryaw7 
Username = aryaw7

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>echo Password length check: 
Password length check:

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>echo ****   | findstr /R "." 
**** 
[Pipeline] }
[Pipeline] // withCredentials
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Docker Build)
[Pipeline] tool
[Pipeline] envVarsForTool
[Pipeline] withEnv
[Pipeline] {
[Pipeline] bat

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>docker build -t aryaw7/employee-sys:3 . 
#0 building with "default" instance using docker driver

#1 [internal] load build definition from Dockerfile
#1 transferring dockerfile: 748B 0.1s done
#1 DONE 0.4s

#2 [internal] load metadata for docker.io/library/eclipse-temurin:17-jdk-alpine
#2 ...

#3 [internal] load metadata for docker.io/library/eclipse-temurin:17-jre-alpine
#3 DONE 3.1s

#2 [internal] load metadata for docker.io/library/eclipse-temurin:17-jdk-alpine
#2 DONE 3.1s

#4 [internal] load .dockerignore
#4 transferring context: 2B done
#4 DONE 0.3s

#5 [internal] load build context
#5 DONE 0.0s

#6 [build 1/8] FROM docker.io/library/eclipse-temurin:17-jdk-alpine@sha256:cf02686befe8e1fc3b00da25458bf92d53013b4c358d4a2245ff50e0d81b753a
#6 resolve docker.io/library/eclipse-temurin:17-jdk-alpine@sha256:cf02686befe8e1fc3b00da25458bf92d53013b4c358d4a2245ff50e0d81b753a
#6 resolve docker.io/library/eclipse-temurin:17-jdk-alpine@sha256:cf02686befe8e1fc3b00da25458bf92d53013b4c358d4a2245ff50e0d81b753a 0.8s done
#6 DONE 1.0s

#7 [stage-1 1/3] FROM docker.io/library/eclipse-temurin:17-jre-alpine@sha256:88c0002860cda56384d5ed3b2da4d0d9a2b44dc2ee4dc02344be985bd8b524bc
#7 resolve docker.io/library/eclipse-temurin:17-jre-alpine@sha256:88c0002860cda56384d5ed3b2da4d0d9a2b44dc2ee4dc02344be985bd8b524bc 0.7s done
#7 DONE 1.0s

#5 [internal] load build context
#5 transferring context: 1.84kB 0.0s done
#5 DONE 0.3s

#8 [build 2/8] WORKDIR /app
#8 CACHED

#9 [build 5/8] RUN chmod +x mvnw
#9 CACHED

#10 [build 6/8] RUN ./mvnw dependency:go-offline
#10 CACHED

#11 [stage-1 2/3] WORKDIR /app
#11 CACHED

#12 [build 4/8] COPY .mvn .mvn
#12 CACHED

#13 [build 8/8] RUN ./mvnw clean package -DskipTests
#13 CACHED

#14 [build 3/8] COPY pom.xml mvnw ./
#14 CACHED

#15 [build 7/8] COPY src ./src
#15 CACHED

#16 [stage-1 3/3] COPY --from=build /app/target/Employee_sys-*.jar app.jar
#16 CACHED

#17 exporting to image
#17 exporting layers done
#17 exporting manifest sha256:256ca40ad2ff53698eb89a0299e592e1feafe440148cd66d41cc8fb40182ca55 0.1s done
#17 exporting config sha256:0b9f6564157a7917a06801e9c5f80ba1df117c8468f5e37e38ea3b93c35fef7a
#17 exporting config sha256:0b9f6564157a7917a06801e9c5f80ba1df117c8468f5e37e38ea3b93c35fef7a 0.2s done
#17 exporting attestation manifest sha256:4896989c29d3b5fe2e3932ba0f9322cb8b9e0d19a53e990fd89d33dabe7ffc09
#17 exporting attestation manifest sha256:4896989c29d3b5fe2e3932ba0f9322cb8b9e0d19a53e990fd89d33dabe7ffc09 1.0s done
#17 exporting manifest list sha256:6dcd0fe262219645a22f753651f355187391426587fa06ba9aa33cf607012d4b
#17 exporting manifest list sha256:6dcd0fe262219645a22f753651f355187391426587fa06ba9aa33cf607012d4b 0.4s done
#17 naming to docker.io/aryaw7/employee-sys:3
#17 naming to docker.io/aryaw7/employee-sys:3 0.1s done
#17 unpacking to docker.io/aryaw7/employee-sys:3 0.1s done
#17 DONE 2.6s
WARNING: current commit information was not captured by the build: git was not found in the system: exec: "git.exe": executable file not found in %PATH%
[Pipeline] bat

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>docker tag aryaw7/employee-sys:3 aryaw7/employee-sys:latest 
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Docker Push)
[Pipeline] tool
[Pipeline] envVarsForTool
[Pipeline] withEnv
[Pipeline] {
[Pipeline] withCredentials
Masking supported pattern matches of %DOCKER_PASSWORD%
[Pipeline] {
[Pipeline] bat

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>echo Logging into Docker Hub... 
Logging into Docker Hub...

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>echo **** 1>pass.txt 

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>docker login -u aryaw7 --password-stdin  0<pass.txt 
Login Succeeded

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>if 0 NEQ 0 exit /b 0 

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>del pass.txt 

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>echo Login successful 
Login successful

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>docker push aryaw7/employee-sys:3 
The push refers to repository [docker.io/aryaw7/employee-sys]
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
09f01c4101f5: Waiting
ee8875ec6b8d: Waiting
ee8875ec6b8d: Waiting
19f02a34e012: Waiting
6a0ac1617861: Waiting
070a7b9fef91: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
19f02a34e012: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
19f02a34e012: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
19f02a34e012: Waiting
6a0ac1617861: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
19f02a34e012: Waiting
775c53a23a89: Waiting
19f02a34e012: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
19f02a34e012: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
19f02a34e012: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
ee8875ec6b8d: Pushed
4f4fb700ef54: Pushed
6a0ac1617861: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
775c53a23a89: Waiting
070a7b9fef91: Pushed
19f02a34e012: Pushed
6b0f9a83cd25: Pushed
6a0ac1617861: Pushed
775c53a23a89: Pushed
09f01c4101f5: Pushed
3: digest: sha256:6dcd0fe262219645a22f753651f355187391426587fa06ba9aa33cf607012d4b size: 856

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>docker push aryaw7/employee-sys:latest 
The push refers to repository [docker.io/aryaw7/employee-sys]
ee8875ec6b8d: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
ee8875ec6b8d: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
ee8875ec6b8d: Waiting
09f01c4101f5: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
ee8875ec6b8d: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
ee8875ec6b8d: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
ee8875ec6b8d: Waiting
070a7b9fef91: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
ee8875ec6b8d: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
ee8875ec6b8d: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
775c53a23a89: Waiting
6b0f9a83cd25: Waiting
ee8875ec6b8d: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
09f01c4101f5: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
ee8875ec6b8d: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
ee8875ec6b8d: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
ee8875ec6b8d: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
775c53a23a89: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
ee8875ec6b8d: Layer already exists
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
775c53a23a89: Layer already exists
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
6a0ac1617861: Waiting
6b0f9a83cd25: Waiting
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
6b0f9a83cd25: Layer already exists
070a7b9fef91: Waiting
19f02a34e012: Waiting
4f4fb700ef54: Waiting
09f01c4101f5: Waiting
6a0ac1617861: Waiting
19f02a34e012: Already exists
4f4fb700ef54: Layer already exists
09f01c4101f5: Layer already exists
6a0ac1617861: Waiting
070a7b9fef91: Waiting
070a7b9fef91: Waiting
6a0ac1617861: Waiting
6a0ac1617861: Layer already exists
070a7b9fef91: Layer already exists
latest: digest: sha256:6dcd0fe262219645a22f753651f355187391426587fa06ba9aa33cf607012d4b size: 856

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>docker logout 
Removing login credentials for https://index.docker.io/v1/
[Pipeline] }
[Pipeline] // withCredentials
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Deploy)
[Pipeline] tool
[Pipeline] envVarsForTool
[Pipeline] withEnv
[Pipeline] {
[Pipeline] bat

C:\ProgramData\Jenkins\.jenkins\workspace\emp_pipe>docker stop springboot-app   || exit 0 
Error response from daemon: No such container: springboot-app
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Declarative: Post Actions)
[Pipeline] echo
Pipeline completed successfully!
[Pipeline] }
[Pipeline] // stage
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // node
[Pipeline] End of Pipeline
Finished: SUCCESS
