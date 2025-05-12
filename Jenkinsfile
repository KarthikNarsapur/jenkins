pipeline {
    agent any

    environment {
        // You can define environment variables here if needed
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the repository
                git branch: "${BRANCH_NAME}", url: "${GITHUB_REPO_URL}"
            }
        }

        stage('Build') {
            steps {
                // Run your build or any other command
                echo 'Building the project...'
                sh './build.sh'  // This assumes you have a build.sh script
            }
        }

        stage('Test') {
            steps {
                // Run tests if any
                echo 'Running tests...'
                sh './run-tests.sh'  // This assumes you have a run-tests.sh script
            }
        }

        stage('Deploy') {
            steps {
                // Deploy the project
                echo 'Deploying the project...'
                sh './deploy.sh'  // This assumes you have a deploy.sh script
            }
        }
    }

    post {
        success {
            echo 'Build was successful!'
        }
        failure {
            echo 'Build failed.'
        }
    }
}
