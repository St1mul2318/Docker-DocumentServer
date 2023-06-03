pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Start docker compose') {
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
