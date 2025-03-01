pipeline {
  agent any
  stages {
    stage('pull code') {
      parallel {
        stage('Pull code by web ui') {
          steps {
            sh 'echo "git code"'
          }
        }

        stage('Pull code by tigger') {
          steps {
            sh 'echo "git by tigger"'
          }
        }

      }
    }

    stage('Building and scanf') {
      parallel {
        stage('Building and scanf') {
          steps {
            sh 'echo "run build"'
          }
        }

        stage('Scan code') {
          steps {
            sh 'echo "scan code"'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        sh '''echo "deploy "
echo "go run main.go"'''
      }
    }

  }
}