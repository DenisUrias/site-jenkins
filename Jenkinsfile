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
            agent {
                dockerfile{
                    additionalBuildArgs '--tag SitePrincipal'
                    filename 'Dockerfile'
                    dir '.'
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
