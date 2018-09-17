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
        echo " echoing ${params.TagValue}"
        echo " echoing ${params.DeployType}"
        echo " echoing ${params.Env}"
        mail(subject: 'test', to: 'ranjeetkumar.singh@zimmerbiomet.com', body: 'test', from: 'jenkins@zimmerbiomet.com')
        bat 'mkdir checkoutcode'
        bat 'svn checkout ${params.TagValue}'
      }
    }
  }
  parameters {
    string(name: 'TagValue', defaultValue: 'v1.0', description: 'Give tag value')
    choice(name: 'DeployType', choices: '''ear-only
full''', description: 'Choose Deployment Type')
    choice(name: 'Env', choices: '''QA
PROD''', description: 'Give Env value')
  }
}
