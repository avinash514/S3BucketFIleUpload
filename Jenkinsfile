pipeline {
	agent any
	tools { 
        maven 'Maven-3.6.0' 
        }
	stages {
	    
	    stage('Checkout'){
	        steps{
				println "Checkout Stage"
				
        //checkout scm
				//checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'GITHUB', url: 'https://github.com/avinash514/S3BucketFIleUpload.git']]])
				script{
					sampleStage();
					sonarBuild();
				}
			}
		}
		
		stage('Build'){
			steps{
				println "Build Stage"
				sh 'mvn clean install -Dmaven.test.skip=true'
			}
		}
		stage('Sonar Build'){
		      steps{
		      	println "This is Sonar Build Stage"
		      }
		      }
}
}

def sampleStage(){
	println "This is Sample stage"
	checkout scm
	println "Hi Hema"
}

def sonarBuild(){
	println "This is Sonar Build Method"
}
