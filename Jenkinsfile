pipeline {
	 agent {label 'master'}
	 options { skipDefaultCheckout() }
         stages {
           stage('CleanWorkspace') 
		 {
             steps {
		    cleanWs()
	           }
	         }
	    stage('Checkout')
		 { 
	      steps {    
		    checkout([$class: 'GitSCM', branches: [[name: '*/main']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/NiluPriya/ASP.NetProject.git']]])
		    }
		 }
            stage('Build') 
		 {
              steps {
                    bat "\"${tool 'MSBuild'}\" TestProject.sln /p:Configuration=Debug"
                    }
    	          }
               }
	
           }
