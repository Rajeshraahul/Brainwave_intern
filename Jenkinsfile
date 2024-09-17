pipeline {
    agent any

    stages {
        stage('Pull Code From GitHub') {
            steps {
                git 'https://github.com/Rajeshraahul/Brainwave_intern.git'
            }
        }
        stage('Build the Docker image') {
            steps {
                sh 'sudo docker build -t intern /var/lib/jenkins/workspace/brainwave'
                sh 'sudo docker tag intern rajeshraahul/intern:latest'
                sh 'sudo docker tag intern rajeshraahul/intern:${BUILD_NUMBER}'
            }
        }
        stage('Push the Docker image') {
            steps {
                sh 'sudo docker image push rajeshraahul/intern:latest'
                sh 'sudo docker image push rajeshraahul/intern:${BUILD_NUMBER}'
            }
        }
        stage('Deploy on Kubernetes') {
            steps {
                sh 'sudo kubectl apply -f /var/lib/jenkins/workspace/brainwave/pod.yaml'
                sh 'sudo kubectl rollout restart deployment loadbalancer-pod'
            }
        }
    }
}       
