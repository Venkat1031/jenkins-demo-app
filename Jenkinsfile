pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t jenkins-demo-app .'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy stage (optional)'
                echo 'Here you could push to DockerHub or run container'
            }
        }
    }
}
