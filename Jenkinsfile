pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh './gradlew assemble'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                sh './gradlew test'
            }
        }
    }
    post {
        always {
            echo 'Pipeline completed!'
        }
    }
}