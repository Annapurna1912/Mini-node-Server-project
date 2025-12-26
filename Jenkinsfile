pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                echo 'Node.js app ready'
            }
        }

        stage('Run') {
            steps {
                sh 'node index.js & sleep 5'
            }
        }
    }

    post {
        success {
            echo '✅ Node.js Jenkins build SUCCESS'
        }
        failure {
            echo '❌ Node.js Jenkins build FAILED'
        }
    }
}
