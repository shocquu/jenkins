pipeline {
    agent none
    stages {
        stage('Clone') {
            steps {
                sh "docker build --no-cache --force-rm -t Dockerfile.clone ."
            }
        }
        stage('Build') {
            steps {
                sh "docker build --no-cache --force-rm -t Dockerfile.build ."
            }
        }
        stage('Test') {
            steps {
                sh "docker build --no-cache --force-rm -t Dockerfile.test ."
            }
        }
        stage('Deploy') {
            steps {
                sh "echo deploy"
            }
        }
    }
}