pipeline {
    agent any
    
    stages {
        stage('Checkout First Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/ahmedm-sallam/FileListerPipeline.git'
            }
        }
        stage('Execute Script from First Repo') {
            steps {
                // Ensure the script is executable and run it
                sh 'chmod +x list_files.sh'
                sh './list_files.sh'
            }
        }
        stage('Checkout Second Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/ahmedm-sallam/repo2.git'
            }
        }
        stage('Execute Script from Second Repo') {
            steps {
                // Ensure the script is executable and run it
                sh 'chmod +x pwd.sh'
                sh './pwd.sh'
            }
        }
    }
}
