pipeline {
    agent any  // Run on any available agent

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g+ -o hello1_exec hello1.cpp'  //instead of g++
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './hello1_exec'  // Execute the compiled program
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy step - Add actual deployment commands here"
            }
        }
    }

    post {
        failure {
            echo "Pipeline failed!"  // Display message if pipeline fails
        }
    }
}
