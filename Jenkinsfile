pipeline {
    agent any

    stages {
        stage('Stage 1') {
            steps {
                bat 'echo Hello from GitHub Jenkinsfile'
            }
        }

        stage('Stage 2') {
            steps {
                bat 'echo Jenkins is pulling code from GitHub'
            }
        }

        stage('Stage 3') {
            steps {
                bat 'echo GitHub + Jenkins pipeline SUCCESS'
            }
        }
    }
}
