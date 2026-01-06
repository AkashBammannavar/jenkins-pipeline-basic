pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Code pulled from GitHub'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t cd-demo-app .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat '''
                docker stop cd-demo || exit 0
                docker rm cd-demo || exit 0
                docker run --name cd-demo cd-demo-app
                '''
            }
        }
    }

    post {
        success {
            echo 'CD Pipeline completed successfully'
        }
    }
}
