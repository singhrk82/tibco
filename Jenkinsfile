pipeline {
  agent any
  
  parameters {
  string(name:'TagValue',defaultValue:'v1.0',description:'Give tag value')  
  }
  
  stages {
    stage('Build') {
      agent {
        node {
          label 'master'
        }

      }
      steps {
        mail(subject: 'test', to: 'ranjeetkumar.singh@zimmerbiomet.com', body: 'test', from: 'jenkins@zimmerbiomet.com')
        sh 'git checkout v1.0'
      }
    }
  }
}
