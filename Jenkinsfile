pipeline {
    agent any
	
      stages{
	stage('Checkout'){
          steps{
	    git branch: 'main',
		credebtialId:'jenkins-docker'
		url: 'https://github.com/KhanwaleedAbbas/jenkins-docker-ci.git'

			}
		}
	stage('Build Docker Image'){
	  steps{
            sh 'docker compsoe build'
	        }
	     }

	stage('Run Container'){
	   steps {
	    sh 'docker compose up -d
	     }
	}

	stage('Cleanup') {
	  steps{
	sh 'docker compose down' 
	 }
	}
   }
}
