pipeline {
    agent {
        any { image 'golang' }
    }
    stages {
        stage('Test') {
            steps {
                sh 'go version'
            }
        }
    }
}