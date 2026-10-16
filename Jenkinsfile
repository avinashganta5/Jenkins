
pipeline {
    agent any
    stages {
        stage('Test Suite') {
            steps {
                echo 'Running tests...'
                // Imagine a test fails here
            }
        }
    }
    
    // The post block executes after all stages finish
    post {
        always {
            echo 'This will ALWAYS run, useful for deleting temporary workspace files.'
        }
        success {
            echo 'This only runs if all stages passed perfectly!'
        }
        failure {
            echo 'WARNING: The pipeline has failed. Sending alerts to the DevOps team...'
        }
    }
}
