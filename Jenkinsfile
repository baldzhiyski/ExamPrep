pipeline {
    agent any 
    stages {
        stage('Setup .NET') {
            steps {
                script {
                    // This assumes you have the .NET plugin installed
                    dotnet '6.0' // Specify the desired .NET version
                }
            }
        }
        stage('Restore dependencies') { 
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Dotnet Build') { 
            steps {
                bat 'dotnet build --no-restore'
            }
        }
        stage('Execute Tests') { 
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
