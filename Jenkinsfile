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
            }
        }
    }
    
    post {
        success {
            // Actions to perform after a successful pipeline run
        }
        failure {
            // Actions to perform after a failed pipeline run
        }
    }
}
