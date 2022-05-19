pipeline {
    agent any

    stages {
        stage('Git checkout') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/madhavkrishna118/project.git'
            }
       stage('Create-Image') {
                // Build the images from dockerfile
			      steps {
				        sh 'docker build -t="madhavkrishna118/pipeline:latest" .'
			}
	     stage('Docker-login') {
		        steps {
		                sh 'docker login -u madhavkrishna118 -p Ilvu@143'
			}
	     stage('Dockerpush') {
			      steps {
				            sh 'docker push madhavkrishna118/pipeline '
			}
	}
}     
