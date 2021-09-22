pipeline {
    agent any

    environment {
        VERSION_APP = 'latest'
        IMAGE_NAME = 'sampleapp'
        PORT = 3000
    }

    stages {
        stage('Information') {
            steps {
                sh 'echo bonjour le monde'
            }
        }
    }

    post {
        always {
            sh 'echo after build'
        }
    }
}