pipeline {
			agent none
   
  
  
			stages {								
				stage('Build') {
					agent {label 'master'}
    					steps {
                    bat "\"${tool 'MSBuild'}\" TestProject.sln /p:Configuration=Debug"
                    }
    					    
    					}

				}
			}
