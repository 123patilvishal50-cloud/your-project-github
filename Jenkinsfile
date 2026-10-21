pipeline{
    agent any

    environment {
        VERCEL_TOKEN = credentials('vercel-token')
    }
    stages {
        stage('install') {
            steps {
                bat 'npm install'
            }
        }
        stage('test') {
            steps {
                echo 'skipping tests'
            }
        }
        stage('deploy') {
            steps {
                bat 'npx vercel --token %VERCEL_TOKEN% --prod --yes --token=%VERCEL_TOKEN%'
            }
        }
    }
}