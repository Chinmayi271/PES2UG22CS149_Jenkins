pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    bat 'g++ -o PES2UG22CS149 hello1.cpp'  // Compile hello1.cpp
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    bat 'PES2UG22CS149'  // Run the compiled executable
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'  // Placeholder for deployment
            }
        }
    }

    post {
        failure {
            script {
                echo 'Pipeline failed'  // Display error message if pipeline fails
            }
        }
    }
}
