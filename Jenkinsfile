pipeline { 
	agent any
	tools {
	      maven 'maven393'
	      }
	stages { 
		stage( 'Compile') { 
			steps {
			cd SparkWordCount
			mvn clean compile
			}
		}
		stage( 'Unit Test') { 
			steps {
			cd SparkWordCount
			mvn clean test
			}
		}
		stage( 'Package') { 
			steps {
			cd SparkWordCount
			mvn clean package
			}
		}	
	}
}
