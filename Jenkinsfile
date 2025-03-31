pipeline {
  agent any

  tools {
    jdk 'Java17'
    maven 'Maven3'
  }

  stages {
    stage('Clean up Workspace') {
      steps {
        script {
          // Clean up the workspace before starting the build
          cleanWs()
        }
      }
    }

    stage('Checkout') {
      steps {
        git branch: 'main', credentialsId: 'github', url: 'https://github.com/phu-phurithat/complete-prodcution-e2e-pipeline'
      }
    }

    stage('Build') {
      steps {
        script {
          // Build the project using Maven
          sh 'mvn clean package'
        }
      }
    }
    stage('Test') {
      steps {
        script {
          // Run unit tests using Maven
          sh 'mvn test'
        }
      }
    }
  }
}