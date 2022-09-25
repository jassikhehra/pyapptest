pipeline {
    agent {
        label 'centos7'
    }
    triggers {
        cron('* * * * *')
    }
    stages {
        stage('Build') {
            steps {
            // One or more steps need to be included within the steps block.
            sh 'python app/app.py'
            }
        }
}

}
