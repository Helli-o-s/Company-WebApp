pipeline {
    agent any
    environment {
        JAVA_HOME = 'C:/Program Files/Java/jdk-17' // Ensure this points to Java 17
        PATH = "${JAVA_HOME}/bin:${env.PATH}"
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                bat './gradlew assemble' // For Windows
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                bat './gradlew test' // For Windows
            }
        }
    }
    post {
        always {
            echo 'Pipeline completed!'
        }
    }
}
