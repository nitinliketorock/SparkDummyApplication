pipeline { 
	agent any
	tools {
	      maven 'maven393'
	      }
	stages { 
		stage( 'Compile') { 
			steps {
			cd SparkWordCount
			bat "mvn -Dmaven.test.failure.ignore=true clean compile"
			}
		}
		stage( 'Unit Test') { 
			steps {
			cd SparkWordCount
			bat "mvn -Dmaven.test.failure.ignore=true clean test"
			}
		}
		stage( 'Package') { 
			steps {
			cd SparkWordCount
			bat "mvn -Dmaven.test.failure.ignore=true clean package"
			}
		}	
	}
}
