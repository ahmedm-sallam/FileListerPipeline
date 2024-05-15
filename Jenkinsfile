pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the repository
                git 'https://github.com/ahmedm-sallam/FileListerPipeline.git'
            }
        }
        stage('Execute Script') {
            steps {
                // Execute the bash script
                sh 'chmod +x list_files.sh'
                sh './list_files.sh'
            }
        }
    }
}
