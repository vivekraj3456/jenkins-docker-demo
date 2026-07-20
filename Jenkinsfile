pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/vivekraj3456/jenkins-docker-demo.git'
            }
        }

        stage('Test') {
            steps {
                bat 'if exist index.html echo Application file index.html found'
            }
        }
    }
}