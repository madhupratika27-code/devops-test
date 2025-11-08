pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: '<https://github.com/madhupratika27-code/devops-test.git>'
            }
        }
        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-app .'
            }
        }
        stage('Run Docker Container') {
            steps {
                sh 'docker stop devops-app || true'
                sh 'docker rm devops-app || true'
                sh 'docker run -d -p 3000:3000 --name devops-app devops-app'
            }
        }
    }
}
