pipeline {
  agent any

  stages {
    stage('Start PostgreSQL') {
      steps {
        sh '''
           cd tests
           export POSTGRES_VERSION=10
           export config=postgres.yml
           ./test.sh
         '''
      }
    }
    stage('Start MySQL') {
      steps {
        sh '''
           cd tests
           export MYSQL_VERSION=8
           export config=mysql.yml
           ./test.sh
         '''
      }
    }
  }
}
