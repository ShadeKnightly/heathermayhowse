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
        stage('Deploy') {
            steps {
                sh 'npx netlify-cli deploy --prod --dir=build --site=$NETLIFY_SITE_ID --auth=$NETLIFY_TOKEN'
            }
        }
    }
}