pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                script {
                    echo "Building PES1UG22CS458-1..."
                }
                sh 'g++ mainhello.cpp -o main/hello_exec'
            }
        }
        stage('Test') {
            steps {
                script {
                    echo "Running Tests..."
                }
                sh './main/hello_exec'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
            error 'Pipeline execution stopped due to failure.'
        }
    }
}

