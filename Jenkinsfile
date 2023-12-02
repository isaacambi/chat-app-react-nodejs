pipeline {
    agent any
    stages {

        stage('bringing the containers to live') {

        
            steps {
                sh 'docker-compose up -d'
            }
        }

        stage('putting down containers') {
            steps {
                sh 'docker-compose down'
            }
        }

        stage('removing all docker images') {
            steps {
                sh 'docker rmi $(docker images -q)'
            }
        }
        stage('bringing up the container') {
            steps {
                sh 'docker-compose up -d'
            }
        }

          
    }

}      
