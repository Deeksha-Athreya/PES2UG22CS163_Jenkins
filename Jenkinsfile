pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'cd main && g++ -o hello_pipeline hello.cpp'
                sh 'echo "Build Stage Successful"'
            }
        }
        stage('Test') {
            steps {
                sh 'cd main && ./hello_pipeline'
                sh 'echo "Test Stage Successful"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deployment Successful"'
            }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
