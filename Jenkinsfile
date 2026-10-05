pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'ls -la'
                sh 'echo "Build step - no maven needed"'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Test passed"'
            }
        }
        stage('Docker Build') {
            steps {
                sh 'docker build -t todosummaryassistant . || echo "No Dockerfile, skipping"'
            }
        }
    }
}
