pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the latest code from GitHub
                git url: '', branch: 'main'
            }
        }
        stage('Check Java Version') {
            steps {
                // Check the installed Java version
                sh 'java --version'
            }
        }
        stage('Build') {
            steps {
                // Compile the Java program
                sh 'javac HelloWorld.java'
            }
        }
        stage('Test') {
            steps {
                // Run the Java program
                sh 'java HelloWorld'
            }
        }
    }
}
