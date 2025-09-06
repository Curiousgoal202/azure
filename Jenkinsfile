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
            slackSend channel: '#johncena', message: "✅ Jobsucceeded!:grinning::grinning::grinning::grinning::grinning::grinning::grinning::grinning::grinning::grinning::grinning:"
        }
        failure {
            slackSend channel: '#johncena', message: "❌ Jobfailed!"
        }
    }
}
