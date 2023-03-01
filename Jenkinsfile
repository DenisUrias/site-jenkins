pipeline {
    
    agent any

    stages {
        stage('Build') {

            steps {
                echo 'Building...'
                
            }            
            
            agent {
                dockerfile{
                    additionalBuildArgs '--tag siteprincipal'
                    filename 'Dockerfile'
                    dir '.'
                }
            }
            
//            steps {
//                echo 'Building...'
                
//            }
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
