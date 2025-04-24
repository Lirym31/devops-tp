pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Lirym31/devops-tp.git'
            }
        }
        
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t devops-tp .'
                }
            }
        }
        
        stage('Run Container') {
            steps {
                script {
                    sh 'docker stop devops-tp || true'
                    sh 'docker rm devops-tp || true'
                    sh 'docker run -d -p 3000:3000 --name devops-tp devops-tp'
                }
            }
        }
    }
}
