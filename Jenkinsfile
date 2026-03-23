pipeline {
    agent any

    stages {

        stage('Clone Repository') {
            steps {
               git branch: 'main',
                    url: 'https://github.com/nithya0312-n/jenkins.git',
                    credentialsId: 'admin-neww'
            }
        }

        stage('Run Python Script') {
            steps {
                sh '''
                python3 --version
                python3 app.py
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}

