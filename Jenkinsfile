pipeline {
    environment {
        imagename = "Dockerfile.build"
        dockerImage = ''
    }
    agent any

    stages {
        stage('Building image') {
            steps{
                script {
                    dockerImage = docker.build("svelte-build", "-f Dockerfile.build .") 
                }
            }
        }
        // stage('Clone') {
        //     steps {
        //         sh "docker build --no-cache --force-rm -t Dockerfile.clone ."
        //     }
        // }
        // stage('Build') {
        //     steps {
        //         sh "docker build --no-cache --force-rm -t Dockerfile.build ."
        //     }
        // }
        // stage('Test') {
        //     steps {
        //         sh "docker build --no-cache --force-rm -t Dockerfile.test ."
        //     }
        // }
        // stage('Deploy') {
        //     steps {
        //         sh "echo deploy"
        //     }
        // }
    }
}