pipeline {
    agent any
    stages {
        stage ('Start tests') {
            parallel{
                stage('Start PostgreSQL9') {
                    steps {
                        lock('postgres9') { 
                            sh '''
                                cd tests
                                export POSTGRES_VERSION=9
                                export config=postgres.yml
                                ./test.sh
                            '''
                        }
                    }
                }
                stage('Start PostgreSQL9.5') {
                    steps {
                        lock('postgres9.5') {
                            sh ''' 
                                cd tests
                                export POSTGRES_VERSION=9.5
                                export config=postgres.yml
                                ./test.sh
                            '''
                        }
                    }
                }
                stage('Start PostgreSQL10') {
                    steps {
                        lock('postgres10') {
                            sh ''' 
                                cd tests
                                export POSTGRES_VERSION=10
                                export config=postgres.yml
                                ./test.sh
                            '''
                        }
                    }
                }
                stage('Start PostgreSQL11') {
                    steps {
                        lock('postgres11') {
                            sh ''' 
                                cd tests
                                export POSTGRES_VERSION=11
                                export config=postgres.yml
                                ./test.sh
                            '''
                        }
                    }
                }
                stage('Start PostgreSQL12') {
                    steps {
                        lock('postgres12') {
                            sh ''' 
                                cd tests
                                export POSTGRES_VERSION=12
                                export config=postgres.yml
                                ./test.sh
                            '''
                        }
                    }
                }
                stage('Start MySQL5.7') {
                    steps {
                        lock('mysql5.7') {
                            sh ''' 
                                cd tests
                                export MYSQL_VERSION=5.7
                                export config=mysql.yml
                                ./test.sh
                            '''
                        }
                    }
                }
                stage('Start MySQL8') {
                    steps {
                        lock('mysql8') {
                            sh ''' 
                                cd tests
                                export MYSQL_VERSION=8
                                export config=mysql.yml
                                ./test.sh
                            '''
                        }
                    }
                }
                stage('Start Certificate') {
                    steps {
                        lock('certs') {
                            sh '''
                                cd tests
                                export config=certs-customized.yml
                                for v in ssl=true private_key=mycert.key certificate_request=mycert.csr certificate=mycert.crt SSL_CERTIFICATE_PATH=/var/www/onlyoffice/Data/certs/mycert.crt SSL_KEY_PATH=/var/www/onlyoffice/Data/certs/mycert.key; do
                                    export $v
                                done
                                ./test.sh
                            '''
                        }
                    }
                }
            }
        }
    }
}
