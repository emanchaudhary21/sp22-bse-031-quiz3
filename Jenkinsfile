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
                sh 'javac HelloWorld.java'
            }
        }

        stage('Run') {
            steps {
                sh 'java HelloWorld'
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
