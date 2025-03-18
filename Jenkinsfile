pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the project...'
                    sh 'g++ -o PES1UG22CS438-1 hello.cpp'  // Compile C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running tests...'
                    sh './PES1UG22CS438-1'  // Execute compiled C++ file
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                    sh 'echo "Deployment Successful!"'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'  // Post condition on failure
        }
        success {
            echo 'Pipeline executed successfully'
        }
    }
}
