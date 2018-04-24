pipeline {
	agent any
	stage(‘Unit Tests’) {
		ant -f test.xml -v
    unit ‘reports/*.xml’
	}
	
}
