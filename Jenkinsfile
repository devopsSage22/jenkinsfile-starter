pipeline {
    agent any
    
    environment {
        // Define environment variables (optional)
        // Example: JAVA_HOME = "/path/to/jdk"
    }

    stages {
        stage('Build') {
            steps {
                // Execute the build (for example, compile your code)
                echo 'Building the application...'
                // Example for Maven build (replace with your tool)
                // sh 'mvn clean install'
            }
        }

        stage('Test') {
            steps {
                // Run unit tests or other tests
                echo 'Running tests...'
                // Example for running tests (replace with your test framework)
                // sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the application (could be to a server or container)
                echo 'Deploying the application...'
                // Example deployment script
                // sh './deploy.sh'
            }
        }
    }

    post {
        always {
            // Clean up or notify after build completes
            echo 'Cleaning up...'
        }

        success {
            // Notify success, for example via Slack or email
            echo 'Build was successful!'
        }

        failure {
            // Handle failure (notify via email or other channels)
            echo 'Build failed. Investigate logs for errors.'
        }
    }
}
