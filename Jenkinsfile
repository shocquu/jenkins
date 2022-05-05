pipeline { 
    agent none
    stages {
        stage('Build') {
            agent {
                dockerfile {
                    filename 'Dockerfile.build'
                }
            }
            steps {
                sh 'echo Build'
            }
        }
        stage('Test') {
            agent {
                dockerfile {
                    filename 'Dockerfile.test'
                }
            }
            steps {
                sh 'echo Test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'node --version'
            }
        }
    }
}