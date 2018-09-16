pipeline {
  agent any
  
  parameters {
  string(name:'TagValue',defaultValue:'v1.0',description:'Give tag value')  
  choice(name:'DeployType',choices:'ear-only\nfull',description:'Choose Deployment Type')  
  choice(name:'Env',choices:'QA\nPROD',description:'Give Env value')
  }
  
  stages {
    stage('Build') {
      agent {
        node {
          label 'master'
        }

      }
      steps {
        echo " echoing ${params.TagValue}"
        echo " echoing ${params.DeployType}"
        echo " echoing ${params.Env}"
        mail(subject: 'test', to: 'ranjeetkumar.singh@zimmerbiomet.com', body: 'test', from: 'jenkins@zimmerbiomet.com')
        sh 'git checkout v1.0'
      }
    }
  }
}
