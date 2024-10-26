pipeline {
    agent {
        docker {
            image 'openjdk:11'
            args '-u root:root -v /root/workspace:/workspace'
        }
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/LaViyaan/Helloworld-Jenkins.git'
            }
        }
        stage('Build and Test') {
            steps {
                sh '''
                    javac -d /workspace HelloWorld.java; 
                    java -cp /workspace HelloWorld
                '''
            }
        }
    }
    post {
        always {
            echo 'Pipeline finished.'
        }
    }
}
