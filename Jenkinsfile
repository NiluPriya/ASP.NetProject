pipeline {
			agent any
	options { skipDefaultCheckout() }
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
