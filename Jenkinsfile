pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/TWOJE_REPOZYTORIUM.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building the app..."
                sh 'echo "Build step — np. npm install albo mvn clean package"'
            }
        }

        stage('Test') {
            steps {
                echo "Running tests..."
                sh 'echo "Test step — np. npm test albo mvn test"'
            }
        }

        stage('Deploy to Test Environment') {
            steps {
                echo "Deploying to test environment..."
                sh 'echo "Deploy script running — np. ./deploy.sh"'
            }
        }
    }

    post {
        success {
            echo 'Pipeline zakończony sukcesem!'
        }
        failure {
            echo 'Pipeline zakończony błędem!'
        }
    }
}
