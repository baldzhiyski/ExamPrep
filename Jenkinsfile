pipeline {
    agent any
    stages {
        stage('Setup .NET') {
            steps {
                script {
                    // Make sure the .NET environment is correctly set up
                    dotnet 'restore'
                }
            }
        }
        stage('Build') {
            steps {
                dotnet 'build'
            }
        }
        stage('Test') {
            steps {
                dotnet 'test'
            }
        }
    }
}
