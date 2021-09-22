pipeline {
    agent {
        dockerfile {
            filename 'Dockerfile'
            dir '.'
            label 'my-suprem-test'
            additionalBuildArgs '-t simpleapp:latest'
        }
    }
    stages {
        stage('Test') {
            steps {
                sh 'npm --version'
                sh 'docker run -p 3000:3000 simpleapp:latest'
            }
        }
    }
}