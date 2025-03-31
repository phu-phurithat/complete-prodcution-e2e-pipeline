pipeline {
  agent {
    label 'jenkins-agent'
  }

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
  }
}