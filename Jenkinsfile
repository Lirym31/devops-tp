pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Lirym31/devops-tp.git'
            }
        }
        
        stage('Build') {
            steps {
                sh 'echo "Installing dependencies..."'
                sh 'npm install || echo "npm install would run here"'
            }
        }
        
        stage('Deploy') {
            steps {
                sh 'echo "Starting application..."'
                sh 'echo "Application would run on port 3000"'
                sh 'echo "SIMULATION: Application deployed successfully"'
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
    }
}
