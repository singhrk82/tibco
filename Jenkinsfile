pipeline {
  agent any
  stages {
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
  }
}