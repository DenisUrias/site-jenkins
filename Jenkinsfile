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
            agent any
            steps {
                echo 'Deploying...'
                sh 'docker tag siteprincipal denisurias/siteprincipal:0.1'
                withDockerRegistry([ credentialsId: "dockerhub", url: "" ]){
                    sh 'docker push denisurias/siteprincipal:0.1'
                }
            }
        }
    }
}
