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
                sh '''
                python3 --version
                python3 -m pip --version
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                echo "Python environment verified"
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy Stage'
            }
        }
    }
}