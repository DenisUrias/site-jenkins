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

                echo 'Upando para Docker Hub...'
                sh 'docker tag siteprincipal denisurias/siteprincipal:0.2'
                sh 'docker tag denisurias/siteprincipal:0.2 denisurias/siteprincipal:latest'
                withDockerRegistry([ credentialsId: "dockerhub", url: "" ]){
                    sh 'docker push denisurias/siteprincipal:0.2'
                }

                echo 'Subindo container...'
                sh 'docker-compose up -d'
//                sh 'docker run -d -p 4431:443 -p 81:80 --name siteprincipal --restart always denisurias/siteprincipal:latest'

            }
        }
    }
}
