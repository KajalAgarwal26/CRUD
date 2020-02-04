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
	stage ('Deploy') {
		steps {
			sh '''
             cp -r $WORKSPACE/dist/matrimony /opt/apache-tomcat-9.0.30/webapps
             curl -u admin:admin http://172.31.43.239:8888/manager/reload?path=/build 
             '''
		}
	}
	
}
}
