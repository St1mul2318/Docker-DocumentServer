pipeline {
    agent any
    stages {
        stage('Start PostgreSQL9') {
            steps {
                sh '''
                    cd tests
                    export POSTGRES_VERSION=9
                    export config=postgres.yml
                    ./test.sh
		    sleep 120
                    '''
            }
        }
        stage('Start PostgreSQL9.5') {
            steps {
                sh ''' 
                    cd tests
                    export POSTGRES_VERSION=9.5
                    export config=postgres.yml
                    ./test.sh
                    sleep 20
                    '''
            }
        }
        stage('Start PostgreSQL10') {
            steps {
                sh ''' 
                    cd tests
                    export POSTGRES_VERSION=10
                    export config=postgres.yml
                    ./test.sh
                    sleep 90
                    '''
            }
        }
        stage('Start PostgreSQL11') {
            steps {
                sh ''' 
                    cd tests
                    export POSTGRES_VERSION=11
                    export config=postgres.yml
                    ./test.sh
		    sleep 90
                    '''
            }
        }
        stage('Start PostgreSQL12') {
            steps {
                sh ''' 
                    cd tests
                    export POSTGRES_VERSION=12
                    export config=postgres.yml
                    ./test.sh
		    sleep 90
                    '''
            }
        }
        stage('Start MySQL5.7') {
            steps {
                sh ''' 
                    cd tests
                    export MYSQL_VERSION=5.7
                    export config=mysql.yml
                    ./test.sh
		    sleep 90
                    '''
            }
        }
        stage('Start MySQL8') {
            steps {
                sh ''' 
                    cd tests
                    export MYSQL_VERSION=8
                    export config=mysql.yml
                    ./test.sh
		    sleep 90
                    '''
            }
        }
        stage('Start Certificate') {
            steps {
                sh '''
                    cd tests
                    export config=certs-customized.yml
                    for v in ssl=true private_key=mycert.key certificate_request=mycert.csr certificate=mycert.crt SSL_CERTIFICATE_PATH=/var/www/onlyoffice/Data/certs/mycert.crt SSL_KEY_PATH=/var/www/onlyoffice/Data/certs/mycert.key; do
                        export $v
                    done
		    ./test.sh
                    sleep 90                    
                    '''
            }
        }
    }
}
