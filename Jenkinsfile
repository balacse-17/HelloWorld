pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Checking Python version...'

                bat '"C:\\Users\\WELCOME\\AppData\\Local\\Programs\\Python\\Python310\\python.exe" --version'

                echo 'Running Python application...'

                bat '"C:\\Users\\WELCOME\\AppData\\Local\\Programs\\Python\\Python310\\python.exe" hello.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'

                bat '"C:\\Users\\WELCOME\\AppData\\Local\\Programs\\Python\\Python310\\python.exe" hello.py'
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