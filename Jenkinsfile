pipeline {
    agent any
    stages {
	    stage('gitclone') {
			steps {
				git branch: 'main', url: 'git@github.com:madhavkrishna118/project.git'
			}
		}
            stage('Build') {
			steps {
				sh 'docker build -t="madhavkrishna118/newnginx:latest" .'
			}
		}
	     stage('Docker-login') {
		        steps {
		                sh 'docker login -u madhavkrishna118 -p 9010438019'
			}
	     }
	      stage('Push') {
			steps {
				sh 'docker push madhavkrishna118/newnginx:latest'
			}
		}
}
}
