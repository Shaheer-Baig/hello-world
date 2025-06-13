pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Add your build steps here
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Add your test steps here
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Add your deploy steps here
            }
        }
    }

    post {
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed! Notifying the team...'
            // Add failure-specific steps here, e.g., sending an email or Slack notification
        }
        always {
            echo 'Cleaning up workspace...'
            cleanWs() // Cleans up the workspace after the build
        }
    }
}
