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