pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                echo '🔧 Update from feature branch: Jenkinsfile modified'
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
                bat 'exit /b 1'
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
