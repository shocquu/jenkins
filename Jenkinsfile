pipeline { 
    agent {
        docker { image 'node:171-alpine' }
    }
    stages {
        stage('Build') {
            agent {
                dockerfile {
                    filename 'Dockerfile.build'
                }
            }
        }
        stage('Test') {
            agent {
                dockerfile {
                    filename 'Dockerfile.test'
                }
            }
        }
        stage('Deploy') {
            steps {
                sh 'node --version'
            }
        }
    }
}