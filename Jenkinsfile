pipeline {
    agent any
    tools {
        git 'Default'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout your code from Git or any other SCM tool
                git url: 'https://github.com/reshmabojje/Reshma.git'
            }
        }
        stage('Build') {
            steps {
                // Perform build steps, for example:
                bat 'mvn clean install'
            }
        }
        stage('Test') {
            steps {
                // Run tests, for example:
                bat 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                // Deploy your application, for example:
                bat 'echo Deploying...'
            }
        }
    }

    post {
        success {
            // Actions to perform if the pipeline succeeds
            echo 'Pipeline succeeded!'
        }
        failure {
            // Actions to perform if the pipeline fails
            echo 'Pipeline failed!'
        }
    }
}
