pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking out source code...'
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building the Python application...'
                bat 'python --version'
                bat 'python hello.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'python hello.py'
            }
        }

        stage('Success') {
            steps {
                echo 'Pipeline completed successfully! 🎉'
            }
        }
    }

    post {
        success {
            echo 'BUILD SUCCESSFUL ✅'
        }

        failure {
            echo 'BUILD FAILED ❌'
        }
    }
}