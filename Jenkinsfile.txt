pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Compile the HelloWorld.java file using javac (if you're not using Maven)
                script {
                    bat 'javac helloworld.java'
                }
            }
        }

        stage('Test') {
            steps {
                // Run unit tests (if using Maven, this would be part of the build)
                script {
                    bat 'java helloworld'  // Run the compiled HelloWorld class
                }
            }
        }
    }
}
