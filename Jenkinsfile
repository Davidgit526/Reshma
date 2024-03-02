pipeline {
    agent any
    
    stages {
        stage('Install dependencies') {
            steps {
                sh 'npm install'
            }
        }
        
        stage('Run tests') {
            steps {
                sh 'npm test'
            }
        }
        
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        
        stage('Deploy') {
            steps {
                // Deployment steps go here
                sh 'echo "Deploying the application...." '
            }
        }
    }
    
    post {
        success {
            // Actions to perform after a successful pipeline run
            sh 'echo "Deployment Successfull" '
        }
        failure {
            // Actions to perform after a failed pipeline run
            sh 'echo "Deployment Failed" '
        }
    }
}
