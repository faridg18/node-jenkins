pipeline {
    agent {
        docker {
            image 'node:10-alpine'
            args '-p 3000:3000'
        }
    }
    environment {
        CI = 'true' 
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install && npm run serve'
            }
        }
        stage('Test') { 
            steps {
                sh 'echo "testing 4"' 
            }
        }
    }
}