pipeline { 
	agent any
	tools {
	      maven 'maven393'
	      }
	stages { 
		stage( 'Compile') { 
			steps {
			sh 'cd SparkWordCOunt && mvn clean compile'
			}
		}
		stage( 'Unit Test') { 
			steps {
			sh 'cd SparkWordCOunt && mvn clean test'
			}
		}
		stage( 'Package') { 
			steps {
			sh 'cd SparkWordCOunt && mvn clean package'
			}
		}	
	}
}
