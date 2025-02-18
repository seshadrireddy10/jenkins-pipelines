pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                checkout scm
            }
        }
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Build') {
            steps {
                script {
                    // Build the application
                    echo 'make build'  // Modify this according to your build process
                }
            }
        }

        stage('Unit Test') {
            steps {
                script {
                    // Run unit tests
                    echo 'make test'  // Modify this according to your test process
                }
            }
        }

        stage('Static Code Analysis') {
            steps {
                script {
                    // Run static code analysis
                    echo 'make lint'  // Modify this according to your static analysis tool
                }
            }
        }

        stage('Security Scan') {
            steps {
                script {
                    // Run security scans
                    echo 'make security-scan'  // Modify this according to your security scanning tool
                }
            }
        }
        stage('End') {
            steps {
                echo 'Bye'
                echo 'Pulling...' +  '$GIT_BRANCH' 
                echo 'build num :  ' + env.BUILD_NUMBER
                sh 'echo $GIT_BRANCH'


                 echo 'GIT_COMMIT' %GIT_COMMIT% 
                 
            }
        }
    }
}


    
