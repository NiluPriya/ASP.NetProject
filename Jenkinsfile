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
	
	
	}
}
