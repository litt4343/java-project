properties([pipelineTriggers([githubPush()])])

node('linux') {   
	stage('Unit Tests') {    
		git credentialsId: 'java-project10New1', url: 'https://github.com/litt4343/java-project.git'
		sh 'ant -f test.xml -v' 
		junit 'reports/*.xml'
	}   
	stage('Build') {    
		sh 'ant -f build.xml -v'   
	}  
	stage('Report') {
	        sh 'aws cloudformation describe-stack-resources --stack-name jenkins --region us-east-1' 
	}
}
	  
