pipeline {
	 agent {label 'master'}
	 triggers {
                   githubPush()
                  }
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
	    stage('Notification')
		 {
	      steps {
		      emailext (
                        to: 'priya.nilu1@outlook.com',
                        subject:'Jenkins Notification',
                        body: 'Job Success'
			      )
	            }
		 }
                }
            }
