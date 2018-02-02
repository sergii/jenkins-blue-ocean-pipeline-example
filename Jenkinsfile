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
    stage('Databases') {
      parallel {
        stage('Ping') {
          steps {
            sleep 1
          }
        }
        stage('Connection') {
          steps {
            sleep 1
          }
        }
      }
    }
    stage('Services') {
      parallel {
        stage('internal') {
          steps {
            sleep 1
          }
        }
        stage('external') {
          steps {
            sleep 1
          }
        }
        stage('3rd party') {
          steps {
            sleep 1
          }
        }
      }
    }
    stage('Integration tests') {
      steps {
        sleep 1
      }
    }
  }
}