node {
    def app

    stage('Clone repository') {
        checkout scm
    }

    stage('Build image') {
	sh 'docker-compose up'
    }

    stage('Test image') {
    /*  sh 'docker-compose -f docker-compose.yml run -rm test' */
        
    }

    stage('Push image') {
        docker.withRegistry('https://registry.hub.docker.com', 'docker-hub') {
            app.push("latest")
        }
    }
}
