// Jenkins pipeline for a Java app with SAST scanning

pipeline {
  agent any 
  
  tools {
    // Configure Maven and Java versions used
    maven 'Maven 3.6.3'
    jdk 'Java 8'  
  }

  stages {

    stage('Checkout') {
      steps {
        // Checkout source code from Git repo 
        git 'https://github.com/your-repo/your-java-app.git'
      }
    }

    stage('Build') {
      steps {
        // Build the app with Maven
        sh 'mvn clean install'  
      }
    }

    stage('Test') {
      steps {
        // Run unit tests
        sh 'mvn test' 
      }
    }

    stage('SAST Scan') {
      environment {
        // Configure SonarScanner tool 
        scannerHome = tool 'SonarScanner 4.7' 
      }
      steps {
        withSonarQubeEnv('SonarCloud') {
          // Run SAST scan using SonarScanner  
          sh "${scannerHome}/bin/sonar-scanner -Dsonar.projectKey=asgbuggywebapp -Dsonar.organization=asgbuggywebapp -Dsonar.sources=."
        }
      }
    }

  }
}
