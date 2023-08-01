pipeline { 
	agent any
	tools {
	      maven 'maven393'
	      }
	stages { 
		stage( 'Compile') { 
			steps {
			cd SparkWordCount
			dir
			mvn clean compile
			}
		}
		stage( 'Unit Test') { 
			steps {
			cd SparkWordCount
			dir
			mvn clean test
			}
		}
		stage( 'Package') { 
			steps {
			cd SparkWordCount
			dir
			}
		}	
	}
}
