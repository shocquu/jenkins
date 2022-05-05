pipeline { 
    def devOpsApp
    
    stages { 
        stage('Clone repo') {
            devOpsApp = docker.build("Dockerfile.clone")
        } 
        stage('Build') { 
            // steps { 
            //     script { 
            //         dockerImage = docker.build registry + ":$BUILD_NUMBER"
            //     }
            // }
            devOpsApp = docker.build("Dockerfile.build")
        }
        
        stage('Test image') {    
            devOpsApp.inside {
                sh 'echo "Tests passed"'
            }
        }
        // stage('Push image') {
        //     docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials') {
        //         app.push("${env.BUILD_NUMBER}")
        //         app.push("latest")
        //     }
        // }
        
        // stage('Deploy our image') { 
        //     steps {
        //         script {
        //             docker.withRegistry( '', registryCredential ) {
        //                 dockerImage.push()
        //             }
        //         }
        //     }
        // }
        // stage('Cleaning up') {
        //     steps {
        //         sh "docker rmi $registry:$BUILD_NUMBER"
        //     }
        // }
    }
}