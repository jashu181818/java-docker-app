pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/jashu181818/java-docker-app.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t java-app .'
            }
        }

        stage('Run Container') {
            steps {
                bat 'docker run -d -p 8085:8085 java-app'
            }
        }

    }
}