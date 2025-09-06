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
            slackSend channel: '#johncena', message: "✅ Jobsucceeded!"
        }
        failure {
            slackSend channel: '#johncena', message: "❌ Jobfailed!"
        }
    }
}
