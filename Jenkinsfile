pipeline{
    agent any

    environment {
        PATH = "/usr/local/share/dotnet:${env.PATH}"
    }
    
    stages{
         stage('Restore'){
             steps{
                 echo 'Restoring...'
                 sh 'dotnet restore'
             }
        }
        stage('Build'){
            steps{
                echo 'Building...'
                sh 'dotnet build --no-restore'
            }
        }
        stage('Test'){
            steps{
                echo 'Testing...'
                sh 'dotnet test --no-build --verbosity normal'  
            }
        }
    }
}