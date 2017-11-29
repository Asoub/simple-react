pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Static Analysis') {
      steps {
        sh 'echo "sonarCube"'
      }
    }
    stage('Unit Tests (Karma)') {
      steps {
        sh 'echo "sonaCube"'
      }
    }    
    stage('Functional Tests (BrowserStack)') {
      parallel {
        stage('IE') {
          steps {
            sh 'echo "test IE"'
          }
        }
        stage('Safari') {
          steps {
            sh 'echo "safari"'
          }
        }
        stage('Chrome') {
          steps {
            sh 'Echo "Chrome"'
          }
        }
      }
    }
  }
  environment {
    CI = 'true'
  }
}
