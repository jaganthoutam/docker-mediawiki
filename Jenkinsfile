#!groovy

pipeline {
  agent {
	dockerfile true
 }
 	stage('Push image') {
        docker.withRegistry('https://registry.hub.docker.com', 'docker-hub') {
            app.push("${env.BUILD_NUMBER}")
            app.push("latest")
        }
    }
  }

