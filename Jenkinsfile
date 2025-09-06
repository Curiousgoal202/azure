pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo "Running build steps..."
            }
        }
    }

    post {
        success {
            slackSend channel: '#johncena', message: "✅ Job '${env.JOB_NAME} [#${env.BUILD_NUMBER}]' succeeded!"
        }
        failure {
            slackSend channel: '#johncena', message: "❌ Job '${env.JOB_NAME} [#${env.BUILD_NUMBER}]' failed!"
        }
    }
}
