node ('linux') {
    stage ("Unit Tests") {
     sh 'ant'
     sh 'ant -f test.xml -v'
    }
    stage ("Build") {
     sh 'ant -f build.xml -v'
    }
    
}
	  
