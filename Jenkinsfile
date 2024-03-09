pipeline {
    agent any  // Run on any available agent

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file using shell script (replace with your actual command)
                    sh 'g++ working.cpp -o PES1UG21CS711-1 || echo "Build failed"'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Print output of the compiled program (replace with your actual command)
                    sh './PES1UG21CS711-1 || echo "Test failed"'
                }
            }
        }
        stage('Deploy') {
            // Replace with your actual deployment steps (e.g., copy to server)
            steps {
                script {
                   if (true) 
                {  // Always fail for demonstration
                echo "Error: Deployment failed due to a simulated issue!"
                exit 1  // Exit with non-zero code to mark failure
                } 
                    else {
                echo "Deployment successful (simulated)"  // Optional success message (remove during simulation)
                        }
                }
            }
        }
    }
    // Post-condition: Display "Pipeline failed" on any error
    post {
        failure {
            echo 'Pipeline failed!'
        }
    }
}
