pipeline {
    agent {
        docker {
            image: 'node-14-alpine'
            args : '-p 3000:3000'
        }
    }

    stages {
        stage('Deploy') {
            steps {
                echo 'Install dependencies'
                sh 'npm install'
            }
        }
    }
}