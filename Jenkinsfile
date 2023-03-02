pipeline {
    
    agent any

    stages {
        stage('Build') {

            steps {
                echo 'Building...'
                
            }            
            
            agent {
                dockerfile{
                    additionalBuildArgs '--tag denis.urias/siteprincipal'
                    filename 'Dockerfile'
                    dir '.'
                }
            }
            
//            steps {
//                echo 'Building...'
                
//            }
        }
        
        stage('Test.') {
            steps {
                echo 'Testing...'
            }
        }
        
        stage('Deploy') {
            agent {
                docker {
                    args 'docker tag siteprincipal \'denisurias/siteprincipal:0.1\''
                    args 'docker push 'denisurias/siteprincipal:0.1''
                    registryCredentialsId 'denisurias'
                    registryUrl 'hub.docker.com'
                }
            }
            steps {
                echo 'Deploying...'
//                sh docker tag siteprincipal 'denisurias/siteprincipal:0.1'
//                sh docker push 'denisurias/siteprincipal:0.1'
            }
        }
    }
}
