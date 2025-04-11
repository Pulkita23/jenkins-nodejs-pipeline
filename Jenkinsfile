pipeline {
    agent any

    tools {
        nodejs "NodeJS-18" // Set up in Jenkins Tools config
    }

    stages {
        stage('Clone Repository') {
            steps {
                git credentialsId: 'github-token', url: 'https://github.com/Pulkita23/jenkins-nodejs-pipeline.git', branch: 'main'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'npm test'
            }
        }

        stage('Start App') {
            steps {
                bat 'start /B npm start'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed.'
        }
    }
}


