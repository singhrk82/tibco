pipeline {
  agent any
  stages {
    stage('Checkout') {
      parallel {
        stage('Checkout') {
          agent {
            node {
              label 'master'
            }

          }
          steps {
            mail(subject: 'test', to: 'ranjeetkumar.singh@zimmerbiomet.com', body: 'test', from: 'jenkins@zimmerbiomet.com')
            bat(script: 'C:\\TEMP\\build.bat', returnStatus: true, returnStdout: true, encoding: 'UTF-8')
          }
        }
        stage('Test') {
          agent {
            node {
              label 'master'
            }

          }
          steps {
            echo 'Just a test'
            echo 'test'
          }
        }
      }
    }
  }
}