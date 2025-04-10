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
                sh 'exit 1'
            }
        }
    }
}
