pipeline {
    agent any

    stages {
	    
	    stage('gitclone') {

			steps {
				git 'https://github.com/madhavkrishna118/project.git'
			}
		}
            stage('Build') {

			steps {
				sh 'docker build -t madhavkrishna118:latest .'
			}
		}
	     stage('Docker-login') {
		        steps {
		                sh 'docker login -u madhavkrishna118 -p Ilvu@143'
			}
	     }
	      stage('Push') {

			steps {
				sh 'docker push madhavkrishna118:latest'
			}
		}
}
}
