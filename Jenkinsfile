pipeline {
  agent any
  stages {
    stage('Test') {
      steps {
        echo 'This is unit test'
      }
    }

    stage('build') {
      steps {
        sh '''pwd
ls
cal 2023'''
      }
    }

    stage('testing') {
      parallel {
        stage('testing') {
          steps {
            echo 'This is test'
          }
        }

        stage('QS Check') {
          steps {
            echo 'QA checking'
          }
        }

      }
    }

    stage('Deploy-prod') {
      steps {
        echo 'deploy on prod'
      }
    }

  }
}