node ('linux') {

    stage ("Build") {
     sh "ant -f build.xml -v"
    }
    stage ("Unit Tests") {
     sh "ant -f test.xml -v"
    }
}
	  
