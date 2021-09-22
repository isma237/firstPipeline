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
                sh 'docker build . -t ${IMAGE_NAME}:${VERSION_APP}'
            }
        }
    }

    post {
        always {
            sh 'docker run -p ${PORT}:${PORT} ${IMAGE_NAME}:${VERSION_APP}'
        }
    }
}