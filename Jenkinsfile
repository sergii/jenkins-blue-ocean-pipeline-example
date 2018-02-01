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
  }
  environment {
    Test = '2'
  }
}