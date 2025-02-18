pipeline {
    agent any

    tools {
        nodejs 'NodeJS 16.2' // Use the Node.js version configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/vardhandeepak27/jenkins-demo'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test' // Add tests later if needed
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Building the application..."'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying the application..."'
                // Optional: Add Docker or deployment steps here
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}