pipeline {
  agent any
  stages {
    stage('Build') {
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
    stage('Deploy') {
      agent {
        node {
          label 'VTIBAPPDV02'
        }

      }
      steps {
        bat 'c:\\temp\\deploy.bat'
      }
    }
  }
}