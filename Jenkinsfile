pipeline {
			agent any
   
  
  
			stages {								
				stage('Build') {
					agent {label 'master'}
    					steps {
                    bat "\"${tool 'MSBuild'}\" TestProject.sln /p:Configuration=Debug"
                    }
    					    
    					}

				}
	post {
		failure {  
			emailext body: 'Jenkins Notification', subject: 'Jenkins Job Failed', to: 'priya.nilu1@outlook.com'
		}
	
	}
}
