pipeline {
    agent {
        dockerfile {
            filename 'Dockerfile'
            dir '.'
            additionalBuildArgs '-t simpleapp:latest'
        }
    }

    environment {
        VERSION_APP = 'latest'
        PORT = 3000
    }

    stages {
        stage('Test') {
            steps {
                sh 'node --version'
            }
        }
    }

    post {
        always {
            sh 'docker run -p ${PORT}:${3000} simpleapp:${VERSION_APP}'
        }
    }
}