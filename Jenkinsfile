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
      steps {
        timeout(time: 4) {
          echo 'Integration'
        }
        
      }
    }
  }
  environment {
    Test = '2'
  }
}