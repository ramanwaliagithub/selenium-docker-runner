pipeline{
    agent any
    stages{
        stage("Pull Latest Image"){
			steps{
                sh "docker pull ramandocker009/selenium-docker"
            }
        }
        stage("Start Grid"){
            steps{
                sh "docker-compose up -d hub chrome firefox"
            }
        }
        stage("Run test"){
            steps{
                sh "docker-compose up search-module book-flight-module"
            }
        }
        stage("Stop Grid"){
            steps{
                sh "docker-compose down"
            }
        }
    }
}