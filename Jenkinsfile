pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                bat '''
                py -m pip install --upgrade pip
                py -m pip install -r requirements.txt
                '''
            }
        }

        stage('Test') {
            steps {
                bat '''
                py -m pytest
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Flask Application to Staging...'
            }
        }
    }

    post {
        success {
            echo 'Build Successful!'
        }

        failure {
            echo 'Build Failed!'
        }
    }
}