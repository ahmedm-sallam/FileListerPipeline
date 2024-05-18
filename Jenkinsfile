pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/ahmedm-sallam/FileListerPipeline.git'
            }
        }
        stage('Clone Additional Repo') {
            steps {
                sh 'git clone https://github.com/ahmedm-sallam/repo2.git'
            }
        }
        stage('Execute Script from Additional Repo') {
            steps {
                script {
                    dir('repo2') {
                        // Ensure the script is executable and run it
                        sh 'chmod +x pwd.sh'
                        sh './pwd.sh'
                    }
                }
            }
        }
    }
}
