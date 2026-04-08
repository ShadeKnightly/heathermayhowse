pipeline {
    agent any

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

    }
}