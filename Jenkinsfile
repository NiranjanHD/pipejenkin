pipeline {
	agent any
	
	stages {
	  stage	('compile'){
		steps {
		   withMaven(maven : 'MAVEN_HOME'){
			sh 'mvn clean compile'
		   }
		}
	  }
	  stage	('testing'){
		steps {
		   withMaven(maven : 'MAVEN_HOME'){
			sh 'mvn test'
		   }
		}
	  }
	  stage	('deploy'){
		steps {
		   withMaven(maven : 'MAVEN_HOME'){
			sh 'mvn deploy'
		   }
		}
	  }
	}
}
