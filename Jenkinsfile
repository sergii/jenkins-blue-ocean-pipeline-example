pipeline {
  agent {
    node {
      label 'test'
    }
    
  }
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
        stage('Service Availability') {
          steps {
            echo 'Checking Third Party Services Availability'
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