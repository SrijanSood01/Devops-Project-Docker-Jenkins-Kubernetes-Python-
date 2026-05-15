pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
                git 'https://github.com/SrijanSood01/Devops-Project-Docker-Jenkins-Kubernetes-Python-'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t srijansood01/python-devops-app:v1 .'
            }
        }

        stage('Push Docker Image') {
            steps {
                sh 'docker push srijansood01/python-devops-app:v1'
            }
        }

        stage('Deploy to Kubernetes') {
            steps {
                sh 'kubectl apply -f k8s/'
            }
        }
    }
}