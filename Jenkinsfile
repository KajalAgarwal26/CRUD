pipeline {
   agent any
	stages {
      stage('SCM Checkout') {
         steps {
            git 'https://github.com/KajalAgarwal26/CRUD.git'
		}
	}
	stage('Build') {
		steps {
			
			sh 'npm install'
      sh 'polymer build'
			                     
		
		}
	}
	
}
}
