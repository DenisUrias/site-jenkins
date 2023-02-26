pipeline {
    agent {
        dockerfile{
            filename 'Dockerfile'
            dir '.'
            args '-v /var/run/docker.sock:/var/run/docker.sock'
            args '-v /run:/run'
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
