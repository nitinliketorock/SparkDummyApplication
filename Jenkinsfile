pipeline {
    agent any
    tools {
        maven 'maven393'
    }
    stages {
        stage('Compile') {
            steps {
                cd SparkWordCount
				bat(/"%MVN_HOME%\bin\mvn" -Dmaven.test.failure.ignore clean compile/)
            }
        }
	}
}
