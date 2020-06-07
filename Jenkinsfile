pipeline {

    agent any

    environment {
        PATH='/usr/local/bin:/usr/bin:/bin'
	}

    stages {

       stage('NPM Setup') {
          steps {
             sh 'npm install'
         }
       }

	    

stage('Adding Android Platform') {
	steps {
		sh 'ionic cordova platform add android'
		}
	}
	  
       stage('Android Build') {
          steps {
               sh 'ionic cordova build android'
               
          }
       }


        stage('Publish Android') {
          steps {
              echo "Publish Android"
          }
       }


}
}
