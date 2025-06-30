pipeline {
    agent any

    tools {
        maven 'Maven'  // ✅ This matches your configured Maven installation
    }

    stages {
        stage('Build with Maven') {
            steps {
                bat 'mvn clean compile'  // use `sh` if on Linux/macOS
            }
        }
    }
}
