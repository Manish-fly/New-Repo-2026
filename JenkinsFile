pipeline {
    agent any

    options {
        timestamps()
    }

    stages {
        stage('Checkout') {
            steps {
                echo "Checking out code for branch: ${env.BRANCH_NAME}"
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo "Build stage running on branch: ${env.BRANCH_NAME}"
            }
        }

        stage('Test') {
            steps {
                echo "Test stage running on branch: ${env.BRANCH_NAME}"
            }
        }
    }

    post {
        success {
            echo "Pipeline SUCCESS for branch: ${env.BRANCH_NAME}"
        }
        failure {
            echo "Pipeline FAILED for branch: ${env.BRANCH_NAME}"
        }
    }
}
