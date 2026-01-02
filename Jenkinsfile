pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/your-username/foodhub-devops.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t foodhub-app .'
            }
        }

        stage('Deploy Application') {
            steps {
                sh 'docker compose down || true'
                sh 'docker compose up -d --build'
            }
        }
    }
}
