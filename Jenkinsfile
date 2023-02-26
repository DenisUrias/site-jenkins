pipeline {
    agent {
        dockerfile{
            filename 'Dockerfile'
            dir '.'
            label 'sitePrincipal'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
        }
    
    }

    stages {
        stage('Build') {
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
