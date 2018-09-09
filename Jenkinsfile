pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        mail(subject: 'test', to: 'ranjeetkumar.singh@zimmerbiomet.com', body: 'test', from: 'jenkins@zimmerbiomet.com')
        bat(script: '"c:\\Program Files\\Git\\bin\\git.exe" clone https://github.com/singhrk82/tibco.git', returnStatus: true)
      }
    }
  }
}