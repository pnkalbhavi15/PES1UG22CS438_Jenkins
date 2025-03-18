pipeline {
    agent any

    environment {
        SRN = "PES1UG22CS438" 
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building the C++ application...'
                    sh "g++ -o main/${SRN}-1 main/hello.cpp"  // Compiling with SRN format
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running the application...'
                    sh 'exit 1'  // Running the compiled program
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deployment simulation...'
                    sh 'echo "Deployment Successful!"'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'  // Executes when any stage fails
        }
        success {
            echo 'Pipeline executed successfully'
        }
    }
}
