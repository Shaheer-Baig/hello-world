pipeline {
    agent any

    parameters {
        booleanParam(
            name: 'executeTests', 
            defaultValue: true, 
            description: 'Run tests during the pipeline build?'
        )
    }

    stages {
        stage('Setup') {
            steps {
                echo 'Setting up the build environment...'
            }
        }

        stage('Build') {
            steps {
                echo 'Building the project...'
            }
        }

        stage('Test') {
            when {
                expression { params.executeTests }
            }
            steps {
                echo 'Running tests...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
            }
        }
    }
}
