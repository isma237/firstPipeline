pipeline {
    agent { dockerfile true }
    stages {
        stage('Test') {
            steps {
                sh 'npm --version'
                sh 'curl http://localhost:3000'
            }
        }
    }
}