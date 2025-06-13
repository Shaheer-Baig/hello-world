pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'echo "Build process completed!"'
            }
        }

        stage('Test') {
            when {
                allOf {
                    expression { env.BRANCH_NAME == 'main' } // Run only on 'main' branch
                    not {
                        expression { env.SKIP_TESTS == 'true' } // Skip if SKIP_TESTS is true
                    }
                }
            }
            steps {
                echo 'Testing...'
                sh 'echo "Running test cases!"'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'echo "Deployment process completed!"'
            }
        }
    }
}
