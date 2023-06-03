pipeline {
    agent {
         docker { image 'ubuntu:latest' }
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
                sh '''
		  cat /etc/os-release
                '''
            }
        }
     }
}
