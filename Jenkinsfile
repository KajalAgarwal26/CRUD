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
             cp -r $WORKSPACE/CRUDUI/build/es6-bundled /opt/apache-tomcat-9.0.30/webapps
             curl -u admin:admin http://13.235.243.117:8888/manager/reload?path=/build 
             '''
		}
	}
	
}
}
