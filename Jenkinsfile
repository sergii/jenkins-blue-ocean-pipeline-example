pipeline {
  agent none
  stages {
    stage('Check code quality') {
      steps {
        echo 'Code is OK'
      }
    }
    stage('Unit tests') {
      steps {
        echo 'Test are OK'
      }
    }
    stage('Integration tests') {
      parallel {
        stage('Integration tests') {
          agent {
            node {
              label 'alpha'
            }
            
          }
          environment {
            alpha = 'alpha'
          }
          steps {
            timeout(time: 4) {
              echo 'Integration'
            }
            
          }
        }
        stage('Availability') {
          steps {
            sleep 1
          }
        }
        stage('Databases') {
          steps {
            sleep 1
          }
        }
        stage('Services') {
          steps {
            sleep 1
          }
        }
      }
    }
  }
  environment {
    Test = '2'
  }
}