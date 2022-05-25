pipeline {
  agent {
    docker {
      image 'node:6-alpine'
    }

  }
  stages {
    stage('Build') {
      parallel {
        stage('Build') {
          steps {
            sh 'npm install'
          }
        }

        stage('Test') {
          steps {
            sh './jenkins/scripts/test.sh'
          }
        }

      }
    }

  }
}