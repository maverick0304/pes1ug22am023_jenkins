pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo "Building the C++ file..."
                    sh 'g++ -o PES1UG22AM023-1 main/hello.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo "Testing the compiled file..."
                    sh './PES1UG22AM023-1'
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo "Deploying the application..."
                    sh 'echo "Deployment step goes here"'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}