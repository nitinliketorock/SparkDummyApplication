pipeline { 
	def mvnHome
    stage('Preparation') { 
        mvnHome = tool 'maven393'
    }
	stages { 
		stage( 'Compile') { 
			steps {
			withEnv(["MVN_HOME=$mvnHome"]) {
					cd SparkWordCount
					bat(/"%MVN_HOME%\bin\mvn" -Dmaven.test.failure.ignore clean compile/)
				}
			}
		}
		stage( 'Unit Test') { 
			steps {
			withEnv(["MVN_HOME=$mvnHome"]) {
					cd SparkWordCount
					bat(/"%MVN_HOME%\bin\mvn" -Dmaven.test.failure.ignore clean test/)
				}
			}
		}
		stage( 'Package') { 
			steps {
			withEnv(["MVN_HOME=$mvnHome"]) {
					cd SparkWordCount
					bat(/"%MVN_HOME%\bin\mvn" -Dmaven.test.failure.ignore clean package/)
				}
			}
		}	
	}
}
