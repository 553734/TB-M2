pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build Frontend') {
            steps {
                script {
                    // Full path to dotnet on Windows (default path)
                    def dotnetPath = 'C:\\Program Files\\dotnet\\dotnet.exe'

                    // Check the .NET version and path
                    sh "${dotnetPath} --version"
                    
                    // Build the .NET project
                    dir('frontend/EasyDevOps') {
                        sh "${dotnetPath} build"
                    }
                }
            }
        }
    }
}
