pipeline {
    agent any

    tools {
        maven 'Maven3' // Must match Maven name in Jenkins -> Global Tool Configuration
    }

    stages {
        stage('Build with Maven') {
            steps {
                bat 'mvn clean compile' // use `sh` if on Linux/macOS
            }
        }
    }
}
