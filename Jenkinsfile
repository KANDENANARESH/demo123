pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git url: 'file:///home/youruser/path-to/node-ci-app'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build') {
            steps {
                echo 'Build successful!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Simulating deployment...'
                // e.g., copy files, restart service, etc.
            }
        }
    }

    post {
        success {
            echo 'CI/CD Pipeline Completed Successfully!'
        }
        failure {
            echo 'Something went wrong.'
        }
    }
}

