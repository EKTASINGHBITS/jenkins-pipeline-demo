pipeline {
    agent any

tools {
    nodejs "Node23" // match the name you gave in Tools config
}

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
    
       stage('Approval for Production Deploy') {
           steps {
              input message: 'Approve deployment to production?', ok: 'Deploy Now'
          }
       }

stage('Production Deploy') {
    steps {
        echo 'Deploying to production environment...'
        bat 'echo Deploying to PRODUCTION environment'
    }
}


        stage('Success Simulation') {
    steps {
        echo 'Simulating success now...'
        bat 'echo This used to fail, but now it succeeds.'
    }
}

    }
}
