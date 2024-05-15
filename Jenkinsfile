pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/ahmedm-sallam/FileListerPipeline.git'
            }
        }
        stage('Execute Script') {
            steps {

                bat 'list_files.bat'
            }
        }
    }
}