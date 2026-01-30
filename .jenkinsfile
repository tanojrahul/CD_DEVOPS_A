pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application...'
                python sample.py
                bat 'echo Build completed'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                bat 'echo Tests passed'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                bat 'echo Deploy successful'
            }
        }
    }

    post {
        success {
            echo 'Pipeline SUCCESS !'
        }
        failure {
            echo 'Pipeline FAILED !'
        }
    }
}
