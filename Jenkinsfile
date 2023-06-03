pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('2-Stage') {
            steps {
                sh '''
                  ls -al
                '''
            }
        }
     }
}
