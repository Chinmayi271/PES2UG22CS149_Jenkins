pipeline {
    agent any  // RUN on any available agent

   stage('Build') {
    steps {
        script {
            sh 'gpp -o hello1_exec hello1.cpp'  // Intentional error: 'gpp' instead of 'g++'
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
            echo "Pipeline failed"  // Display message if pipeline fails
        }
    }
}
