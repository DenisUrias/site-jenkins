pipeline {
    agent any

    stages {
        stage('Build') {
            agent {
      	        docker {
                    image 'siteprincipal'
                }
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
