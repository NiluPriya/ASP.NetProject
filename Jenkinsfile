pipeline {
			agent none
   
  
  
			stages {								
				stage('Build') {
					agent {label 'master'}
    					steps {
                    echo "Test Stage"
                    }
    					    
    					}
				 stage('Stage 2') {
      agent {label 'Slave1'}
      steps {
          echo "I am Slave"
      }
    }
				}
			}
