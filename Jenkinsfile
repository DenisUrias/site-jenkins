pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
#		docker build . -t site-jenkins
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
