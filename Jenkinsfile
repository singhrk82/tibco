pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        build(job: 'Build', quietPeriod: 8)
      }
    }
  }
}