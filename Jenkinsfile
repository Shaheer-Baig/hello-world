pipeline {
    agent any

    parameters {
        booleanParam(name: 'executeTests', defaultValue: true, description: 'Run the test stage?')
        string(name: 'DEPLOY_ENV', defaultValue: 'staging', description: 'Enter deployment environment')
        choice(name: 'BUILD_TYPE', choices: ['debug', 'release'], description: 'Choose build type')
    }

    stages {
        stage('Build') {
            steps {
                echo "🔨 Starting ${params.BUILD_TYPE} build"
                echo "Build completed successfully."
            }
        }

        stage('Test') {
            when {
                expression { return params.executeTests }
            }
            steps {
                echo "✅ Running unit tests..."
                echo "Tests executed successfully."
            }
        }

        stage('Deploy') {
            steps {
                echo "🚀 Deploying to ${params.DEPLOY_ENV} environment"
            }
        }
    }

    post {
        always {
            echo '📋 Pipeline execution finished.'
        }
    }
}
