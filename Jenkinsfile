pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
      	        docker {
                    image 'siteprincipal'
                }
            }
            steps {
                echo 'Building...'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
