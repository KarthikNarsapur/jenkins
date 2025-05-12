pipeline {
    agent any
    parameters {
        string(name: 'GITHUB_REPO_URL', defaultValue: 'https://github.com/example/repo.git', description: 'GitHub Repository URL')
        string(name: 'BRANCH', defaultValue: 'main', description: 'Git branch')
        string(name: 'SCRIPT_PATH', defaultValue: 'Jenkinsfile', description: 'Path to the Jenkinsfile')
    }
    stages {
        stage('Checkout') {
            steps {
                script {
                    // Using the parameters set above
                    env.GITHUB_REPO_URL = params.GITHUB_REPO_URL
                    env.BRANCH = params.BRANCH
                    env.SCRIPT_PATH = params.SCRIPT_PATH
                }
            }
        }
    }
}
