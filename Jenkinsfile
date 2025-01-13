pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                checkout scm
            }
        }
        stage('Build Frontend') {
            steps {
                script {
                    // Navigate to the frontend directory and build the .NET project
                    dir('frontend/EasyDevOps') {
                        // Use .NET CLI to build the project
                        sh 'dotnet build'
                    }
                }
            }
        }
    }

    post {
        success {
            echo 'Build completed successfully!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
