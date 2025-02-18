pipeline {
    agent any

    tools {
        nodejs 'NodeJS 16.x' // Use the Node.js version configured in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/vardhandeepak27/jenkins-demo'
            }
        }
        stage('Check Node.js Installation') {
            steps {
                bat 'node --version'
                bat 'npm --version'
    }
}

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                bat 'npm test' // Add tests later if needed
            }
        }

        stage('Build') {
            steps {
                bat 'echo "Building the application..."'
            }
        }

        stage('Deploy') {
            steps {
                bat 'echo "Deploying the application..."'
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