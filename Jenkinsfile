pipeline {
  agent {
    docker { image 'ubuntu:22.04' }
  }

  stages {
    stage('Start tests') {
      steps {
        sh '''
           cd tests
           export POSTGRES_VERSION=9.5
           export config=postgres.yml
           ./test.sh
         '''
      }
    }
  }
}
