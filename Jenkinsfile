pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Compile the project
               // sh 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Running Tests...'
                // Run the test cases
               // sh 'mvn test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Placeholder for deployment-specific commands
            }
        }
    }
    post {
        always {
            echo 'Pipeline execution completed.'
        }
        success {
            echo 'Build and tests succeeded!'
        }
        failure {
            echo 'Build or tests failed. Please check the logs.'
        }
    }
}
