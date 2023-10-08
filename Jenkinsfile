pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'This is build'
      }
    }

    stage('Test1') {
      parallel {
        stage('Test1') {
          steps {
            sh '''pwd
date
ls -lrt'''
          }
        }

        stage('Test2') {
          steps {
            echo 'this is test 2'
          }
        }

      }
    }

    stage('Deploy') {
      steps {
        echo 'This is deploy'
      }
    }

    stage('Finaloutput') {
      steps {
        writeFile(file: 'blueocean.txt', text: 'Hi I am blueocean')
      }
    }

  }
  environment {
    name = 'Shweta'
    city = 'banglore'
  }
}