pipeline {
    environment {
        imagename = "svelte-test"
        dockerImage = ''
    }
    agent any

    stages {
        stage('Building image') {
            steps{
                script {
                    dockerImage = docker.build imagename
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