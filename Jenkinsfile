pipeline {
  agent any

  stages {
    stage('Start tests') {
      steps {
        sh '''
           cd tests
           export POSTGRES_VERSION=10
           export config=postgres.yml
           ./test.sh
         '''
      }
    }
  }
}
