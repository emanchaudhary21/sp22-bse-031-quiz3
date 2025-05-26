pipeline {
    agent any

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
}
