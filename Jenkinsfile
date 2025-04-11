pipeline {
    agent any

    tools {
        nodejs "NodeJS-18"  // Ensure you set this in Jenkins settings
    }

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/your-username/jenkins-nodejs-pipeline.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build') {
            steps {
                echo 'Build complete. App is ready.'
            }
        }
    }
}
