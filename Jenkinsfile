pipeline { 
	agent any
	tools {
	      maven 'maven393'
	      }
	stages { 
		stage( 'Compile') { 
			steps {
			sh 'cd SparkWordCount'
			sh 'mvn clean compile'
			}
		}
		stage( 'Unit Test') { 
			steps {
			sh 'cd SparkWordCount' 
			sh 'mvn clean test'
			}
		}
		stage( 'Package') { 
			steps {
			sh 'cd SparkWordCount' 
			sh 'mvn clean package'
			}
		}	
	}
}
