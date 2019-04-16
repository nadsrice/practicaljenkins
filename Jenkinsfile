pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building.......'
      }
    }
    stage('Test') {
      parallel {
        stage('Test') {
          steps {
            echo 'Testing......'
          }
        }
        stage('Test Chrome') {
          steps {
            sh 'echo $testing chrome browser'
          }
        }
        stage('Test Edge') {
          steps {
            sh 'echo $testing echo '
          }
        }
      }
    }
    stage('Deploy to Stage') {
      steps {
        echo 'Deploying to Stage....'
      }
    }
    stage('Deploy to Prod') {
      steps {
        echo 'Deploying to Prod.....'
      }
    }
  }
}