pipeline {
    agent any

    tools {
        nodejs "NodeJS-18" // Set up in Jenkins Tools config
    }

    stages {
        stage('Clone Repository') {
            steps {
                git credentialsId: 'github-token', url: 'https://github.com/Pulkita23/jenkins-nodejs-pipeline.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build App') {
            steps {
                echo '✅ Build finished successfully!'
            }
        }
    }
}




