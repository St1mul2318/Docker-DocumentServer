pipeline {
    agent any
    stages {
        stage('Start PostgreSQL9') {
            blocks {
                block([$class: 'BuildBlockerBlockerProperty', blockingJobs: '*']) { // устанавливаем параметры блокировки                    
                    steps {
                        sh '''
                            cd tests
                            export POSTGRES_VERSION=9
                            export config=postgres.yml
                            ./test.sh
                           '''
                    }
                }
            }
        }
        stage('Start PostgreSQL9.5') {
            blocks {
                block([$class: 'BuildBlockerBlockerProperty', blockingJobs: '*']) { // устанавливаем параметры блокировки                    
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
        stage('Start PostgreSQL10') {
            blocks {
                block([$class: 'BuildBlockerBlockerProperty', blockingJobs: '*']) { // устанавливаем параметры блокировки                    
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
        stage('Start PostgreSQL11') {
            blocks {
                block([$class: 'BuildBlockerBlockerProperty', blockingJobs: '*']) { // устанавливаем параметры блокировки                    
                    steps {
                        sh '''
                            cd tests
                            export POSTGRES_VERSION=11
                            export config=postgres.yml
                            ./test.sh
                           '''
                    }
                }
            }
        }
        stage('Start PostgreSQL12') {
            blocks {
                block([$class: 'BuildBlockerBlockerProperty', blockingJobs: '*']) { // устанавливаем параметры блокировки                    
                        steps {
                        sh '''
                            cd tests
                            export POSTGRES_VERSION=12
                            export config=postgres.yml
                            ./test.sh
                           '''
                    }
                }
            }
        }
        stage('Start MySQL5.7') {
            blocks {
                block([$class: 'BuildBlockerBlockerProperty', blockingJobs: '*']) { // устанавливаем параметры блокировки                    
                    steps {
                        sh '''
                            cd tests
                            export MYSQL_VERSION=5.7
                            export config=mysql.yml
                            ./test.sh
                           '''
                    }
                }
            }
        }
        stage('Start MySQL8') {
            blocks {
                block([$class: 'BuildBlockerBlockerProperty', blockingJobs: '*']) { // устанавливаем параметры блокировки                    
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
        stage('Start Certificate') {
            blocks {
                block([$class: 'BuildBlockerBlockerProperty', blockingJobs: '*']) { // устанавливаем параметры блокировки                    
                    steps {
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
