pipeline {
    agent any

    tools{
        nodejs 'Node20'
    }

    stages {
            stage('Build'){
            steps{
                echo 'Building the application...'
                sh 'npm install'
                sh 'npm run build'
            }
        }
        stage('Test'){
            steps{
                echo 'Running tests...'
                sh 'npm test -- --watchAll=false'
            }
        }
        stage('Deploy'){
            steps{
                echo 'Deploying the application...'
                // Add deployment steps here
                //local 
                sh 'npm run deploy'


            }
        }

    }
}