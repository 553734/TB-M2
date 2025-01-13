pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                checkout scm
            }
        }

        stage('Build Frontend') {
            steps {
                script {
                    // Define the path to dotnet executable
                    def dotnetPath = 'C:\\Program Files\\dotnet\\dotnet.exe'

                    // Navigate to the frontend directory and build the .NET app
                    dir('frontend/EasyDevOps') {
                        // Build the .NET app
                        sh "${dotnetPath} build"
                    }
                }
            }
        }
    }
}
