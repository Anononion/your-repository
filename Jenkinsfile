pipeline {
    agent any
    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Anononion/your-repository.git'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t your-app:latest .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 8081:8080 --name my-app your-app:latest'
            }
        }
    }
}
