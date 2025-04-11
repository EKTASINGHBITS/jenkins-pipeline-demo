pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Installing dependencies...'
                bat 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'npm test'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Simulating deployment...'
                bat 'echo Deploying to dev environment'
            }
        }

        stage('Fail Simulation') {
            steps {
                echo 'This stage will fail...'
                bat 'exit /b 1'
            }
        }
    }
}
