pipeline {
    agent {
        docker { image 'ubuntu:latest' }
    }
    stages {
        stage('Build') {
            steps {
                python app/app.py
            }
        }
    }
}
