pipeline {
    agent {
         docker { image 'ubuntu:22.04' }
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
		sh 'ls -al'
            }
        }
        stage('Start docker compose') {
            steps {
                echo "Ubuntu installing successfull"
            }
        }
     }
}
