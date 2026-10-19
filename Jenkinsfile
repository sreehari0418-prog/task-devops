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
                sh 'python3 -m py_compile app.py'
                echo 'Build check passed!'
            }
        }

        stage('Test') {
            steps {
                sh 'python3 app.py'
                echo 'Test stage completed!'
            }
        }
    }
}