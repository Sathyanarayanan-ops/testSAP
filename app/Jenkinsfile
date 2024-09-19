pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                git 'https://github.com/Sathyanarayanan-ops/testSAP.git' // Replace with your repo URL
            }
        }

        stage('Install dependencies') {
            steps {
                sh 'pip install -r requirements.txt || true'
            }
        }

        stage('Run Code') {
            steps {
                sh 'python3 main.py'
            }
        }
    }

    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}
