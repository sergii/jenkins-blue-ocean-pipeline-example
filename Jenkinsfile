pipeline {
  agent none
  stages {
    stage('Code quality') {
      steps {
        echo 'Code is OK'
      }
    }
    stage('Unit tests') {
      steps {
        echo 'Test are OK'
      }
    }
    stage('Availability') {
      parallel {
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
    stage('Integration tests') {
      steps {
        echo 'Integration tests...'
      }
    }
  }
}