pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Kajol2904/Docker.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'ls -l' // See files in the workspace
                sh 'docker build -t my-docker-webapp .'
            }
        }

        stage('Run Docker Container') {
            steps {
                sh 'docker run -d -p 8081:80 my-docker-webapp'
            }
        }
    }
}
