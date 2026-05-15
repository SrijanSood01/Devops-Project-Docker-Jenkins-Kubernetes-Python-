pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git branch: 'main',
                url: 'https://github.com/SrijanSood01/Devops-Project-Docker-Jenkins-Kubernetes-Python-.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat 'docker build -t srijansood/python-devops-app:v1 .'
            }
        }

        stage('Push Docker Image') {
            steps {
                bat 'docker push srijansood/python-devops-app:v1'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                bat 'kubectl apply -f k8s/'
            }
        }
    }
}