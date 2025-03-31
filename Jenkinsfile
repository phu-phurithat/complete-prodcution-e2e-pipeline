pipeline {
  agent {
    label 'jenkins-agent'
  }

  tools {
    maven 'Maven3'
    jdk 'Java17'
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
  }

  stages {
    stage('Checkout') {
      steps {
        git branch: 'main', credentialsId: 'github', url: 'https://github.com/phu-phurithat/complete-prodcution-e2e-pipeline'
      }
    }
  }
}