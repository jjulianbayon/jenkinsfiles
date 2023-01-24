pipeline{
  agent any
stages {
  stage ('Build and package'){
    steps {
        script {
          //begin common code 
          if (fileExists()) {
            def readcounter =    readFile(file: 'version.txt')
            readcounter = readcounter.toInteger() +1
            def version= "Version" + readcounter
            println(version)
            //bat 'mvn package -Dartifactversion=' + "${version}"
            //writeFile(file: 'version.txt',    text:readcounter.toString())
          } //if condition
          else {
            currentBuild.result = "FAILURE" 
          } //else condition
    //end common code
        } //script
        echo "Build and Package Completed" 
      } //steps
    } //stage
  }
}

  
