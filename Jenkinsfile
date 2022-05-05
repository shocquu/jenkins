pipeline {
    agent {
        label 'docker'  # separate agent (launched as JAR on host machine) to avoid running docker inside docker
    } 
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