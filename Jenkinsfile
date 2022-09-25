pipeline {
    agent { 
        node { label 'java-docker-slave' } 
        }
    stages {
        stage('Build') {
            steps {
                python app.py
            }
        }
    }
}
