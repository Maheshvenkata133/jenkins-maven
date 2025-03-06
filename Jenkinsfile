pipeline{
    agent any
    stages{
        stage('Compile & Clean'){
	    steps{
		sh "printenv"
		sh "mvn clean compile"
	    }
	}
	stage ('Test'){
	    steps{
		sh "mvn test"
	   }
	}
	stage ('Deploy'){
	    steps{
		sh "mvn package"
	    }
	}
	stage ('Archiving'){
	    steps{
		archiveArtifacts '**/target/*.jar'
	    }
	}
     }
}
