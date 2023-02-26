pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
                docker {
                    build . 
                }
            }
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
