pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
        stage('Fail Simulation') {
            steps {
                echo 'This stage will fail...'
                sh 'exit 1' // or use bat on Windows: bat 'exit /b 1'
            }
        }
    }

    post {
        success {
            echo '✅ Pipeline completed successfully!'
        }
        failure {
            echo '❌ Pipeline failed. Please check the logs.'
        }
        always {
            echo '🔁 This runs no matter what. Cleaning up...'
        }
    }
}
