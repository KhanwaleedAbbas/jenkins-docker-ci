pipeline {
    agent any
	
      stages{
	stage('Checkout'){
          steps{
	    git branch: 'main',
		credentialsId:'jenkins-docker',
		url: 'https://github.com/KhanwaleedAbbas/jenkins-docker-ci.git'

			}
		}
	stage('Build Docker Image'){
	  steps{
            sh 'docker compose build'
	        }
	     }

	stage('Run Container'){
	   steps {
	    sh 'docker compose up -d'
	     }
	}

	stage('Cleanup') {
	  steps{
	sh 'docker compose down' 
	 }
	}
   }
}
