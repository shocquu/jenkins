pipeline {
    agent any

    stages {

        stage('Clone repo') {
            steps {
                script {
        			docker.build("svelte-cloned", ". -f Dockerfile.clone")
        // 			sh "rm -rf vol_input"
        // 			sh "mkdir vol_input"
        // 			sh "docker run -dt --name node_js --mount src=vol_input,dst=/cloned --mount src=vol_output,dst=/built node:17-alpine"
        // 			sh "ls vol_input"
        		}
            }
        }

	    stage('Build') {
            steps {
                script {
        			def imageBuild = docker.build("svelte-built", ". -f Dockerfile.build")
        			sh "rm -rf shared"
        			sh "mkdir shared"
        			imageBuild.run("-v \$(pwd)/shared:/output")
        			sh "ls shared"
        		}
            }
        }
    
	    stage('Test') {
            steps {
                script {
			        docker.build("sveltejs-test", ". -f Dockerfile.test")
			        sh "echo Testing phase"
		        }
            }
        }

	    stage('Deploy') {
            steps {
                script {			
			        sh "echo Deploy phase"
		        }
            }
        }
    }
}
