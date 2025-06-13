pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                bat 'echo Build process completed!'
            }
        }

        stage('Test') {
            when {
                allOf {
                    expression { env.BRANCH_NAME == 'main' }
                    not {
                        expression { env.SKIP_TESTS == 'true' }
                    }
                }
            }
            steps {
                echo 'Testing...'
                bat 'echo Running test cases!'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                bat 'echo Deployment process completed!'
            }
        }
    }
}
