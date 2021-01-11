pipeline {
			agent any
   stages {
        stage('CleanWorkspace') {
            steps {
		    cleanWs()
	    }
	}
  
  
											
				stage('Build') {
					agent {label 'master'}
    					steps {
                    bat "\"${tool 'MSBuild'}\" TestProject.sln /p:Configuration=Debug"
                    }
    					    
    					}

				}
	
	
	
}
