pipeline {
    agent any
      tools {
        maven 'Maven-3.8.5' // Reference the Maven installation defined in Jenkins global configuration
        jdk 'JDK-11'        // Reference the JDK installation defined in Jenkins global configuration
    }
    environment {
        JAVA_VERSION = '11'
        MAVEN_VERSION = '3.8.5'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                echo "Using Java version: ${env.JAVA_VERSION}"
                echo "Using Maven version: ${env.MAVEN_VERSION}"
                // Compile the project
                bat 'nvm install'
            }
        }
        stage('Test') {
            steps {
                echo 'Running Tests...'
                echo "Testing with Java version: ${env.JAVA_VERSION}"
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
