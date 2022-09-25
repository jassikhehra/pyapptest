pipeline {
    agent {
        label 'centos7'
    }
    triggers { 
        pollSCM('* * * * *') 
        }
    
    stages {
        stage('Build') {
            steps {
            // One or more steps need to be included within the steps block.
            sh 'python app/app.py'
            }
        }
}
    post {
        always {
            echo 'I will always say Hello again!'
            
            emailext body: "${currentBuild.currentResult}: Job ${env.JOB_NAME} build ${env.BUILD_NUMBER}\n More info at: ${env.BUILD_URL}",
            to: "jassikhehra27@gmail.com",
            subject: "Jenkins Build ${currentBuild.currentResult}: Job ${env.JOB_NAME}"
            
        }
    }

}
