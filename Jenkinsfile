pipeline {
	agent any
	tools { 
        maven 'Maven-3.6.0' 
        }
	stages {
	    
	    stage('Checkout'){
	        steps{
				println "Checkout Stage"
				
        checkout scm
				//checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'GITHUB', url: 'https://github.com/avinash514/S3BucketFIleUpload.git']]])
				script{
					sampleStage()
				}
			}
		}
		
		stage('Build'){
			steps{
				println "Build Stage"
				sh 'mvn clean install -Dmaven.test.skip=true'
			}
		}	
}
}

def sampleStage(){
	println "This is Sample stage"
}
