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
	        withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'jenkins-aws-assign10', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) sh 'aws cloudformation describe-stack-resources --stack-name jenkins --region us-east-1' 
	}}
}
	  
