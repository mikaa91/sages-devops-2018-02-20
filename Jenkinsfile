pipeline {
  agent any
  stages {
    stage('Kompilacja') {
      steps {
        sh 'echo \'mvn build\''
      }
    }
    stage('Integration') {
      parallel {
        stage('Integration') {
          steps {
            echo 'Integration test passed !'
          }
        }
        stage('System Test') {
          steps {
            echo 'System Test complete !'
          }
        }
      }
    }
    stage('User Acceptance') {
      steps {
        echo 'BAP signed !'
      }
    }
    stage('Release') {
      steps {
        echo 'Realese Successed !'
      }
    }
  }
}