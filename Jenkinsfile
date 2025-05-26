
---

### ✅ `Jenkinsfile` (Without Maven)

```groovy
pipeline {
    agent any

    tools {
        jdk 'JDK 21'   // This must match the name in Jenkins > Global Tool Configuration
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
