pipeline {
    agent any

    stages {
        stage('Checkout Verification') {
            steps {
                echo 'Repository checked out successfully'
            }
        }

        stage('Maven Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Test Artifact') {
            steps {
                echo 'Checking generated artifact'
                bat 'dir target'
            }
        }
    }

    post {
        success {
            echo 'Pipeline from Git completed successfully'
        }
    }
}