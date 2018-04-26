properties([pipelineTriggers([githubPush()])])

node('linux') {   
	stage('Unit Tests') {    
		git credentialsId: 'java-project10New1', url: 'https://github.com/litt4343/java-project.git'
		sh 'ant -buildfile test.xml' 
		junit 'reports/*.xml'
	}   
	stage('Build') {    
		sh 'ant'   
	}   
}
	  
