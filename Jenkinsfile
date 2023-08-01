pipeline {
    agent any
    tools {
        maven 'maven363'
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
