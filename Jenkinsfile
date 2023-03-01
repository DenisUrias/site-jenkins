pipeline {
    agent any
//    agent {
//        dockerfile{
 //           filename 'Dockerfile'
 //           dir '.'
 //           args '-v /var/run/docker.sock:/var/run/docker.sock'
 //           args '-v /run:/run'
//        }
    
//    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                dockerfile{
                    filename 'Dockerfile'
                    dir '.'
                }
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
