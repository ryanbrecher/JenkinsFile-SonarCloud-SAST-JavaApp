# ![My Skills](https://skillicons.dev/icons?i=jenkins,maven,vscode,java,github)
# JenkinsFile for SonarCloud SAST on Java App

As a DevSecOps engineer, I have been tasked with creating a Jenkinsfile for performing SAST scan on a Java web application using SonarCloud. The Jenkinsfile should include the following stages:

 **Checkout:** Checkout the source code from a Git repository "https://github.com/your-repo/your-node-app.git".

 **Build:** Build the Java application using the "mvn install" command.

 **Test:** Run unit tests on the Node.js application using the "mvn test" command.

 **SAST scan:** Run SAST scan using SonarCloud with the below values:

- Sonar URL = https://sonarcloud.io/
- Sonar Org = javabuggywebapp
- Sonar ProjectKey = javabuggywebapp
- Sonar Login = 93f470b908a46156f5844
