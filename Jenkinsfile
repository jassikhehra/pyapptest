pipeline {
    agent { 
        node { label 'centos7' } 
        }
    stages {
        stage('Build') {
            steps {
                python app/app.py
            }
        }
    }
}
