pipeline {
    agent any
    environment {
        // Variables defined here can be used by any stage
        NEW_VERSION = '1.3.0' 
    }
    stages {
        stage('Build') {
            steps {
                // Output the value of the variable in a string
                echo "Building version ${NEW_VERSION}" 
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post {
        always {
            echo 'Post build condition running'
        }
        failure {
            echo 'Post Action if Build Failed'
        }
    }
}