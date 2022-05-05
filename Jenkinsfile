pipeline { 
    agent {
        dockerfile {
            filename 'Dockerfile.build'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t docker-build -f ./Dockerfile.build .'
            }
        }
        stage('Test') {
            steps {
                sh 'docker build -t docker-build -f ./Dockerfile.test .'
            }
        }
        stage('Deploy') {
            steps {
                sh 'node --version'
            }
        }
    }
}