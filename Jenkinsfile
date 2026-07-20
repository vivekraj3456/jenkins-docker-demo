pipeline {
    agent any

    stages {
        stage('Build Docker Image') {
            steps {
                bat 'docker build -t jenkins-demo .'
            }
        }

        stage('Run Docker Container') {
            steps {
                bat 'docker stop mywebsite || exit 0'
                bat 'docker rm mywebsite || exit 0'
                bat 'docker run -d -p 8081:80 --name mywebsite jenkins-demo'
            }
        }
    }
}