pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "maven393"
    }

    stages {
        stage('Compile') {
            steps {
                 // To run Maven on a Windows agent, use
                 bat "mvn -Dmaven.test.failure.ignore=true clean compile"
            }

        }
		stage('Test') {
            steps {
                 // To run Maven on a Windows agent, use
                 bat "mvn -Dmaven.test.failure.ignore=true clean test"
            }

        }
		stage('Package') {
            steps {
                 // To run Maven on a Windows agent, use
                 bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

        }
    }
}
