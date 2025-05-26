pipeline {
    agent any

    tools {
        jdk 'JDK 21'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                bat 'javac HelloWorld.java'
            }
        }

        stage('Run') {
            steps {
                bat 'java HelloWorld'
            }
        }
    }

    post {
        success {
            echo 'Execution successful!'
        }
        failure {
            echo 'Execution failed.'
        }
    }
}
