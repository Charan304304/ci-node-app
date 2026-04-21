pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Charan304304/ci-node-app.git '
            }
        }
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }
        stage('Run Application') {
            steps {
              bat   'node app.js'
            }
        }
        stage('Run Tests') {
            steps {
                bat 'node test'
            }
        }
    }
    post {
        success{
            echo 'CI Pipeline executed successfully!'
        }
        failure {
            echo 'CI Pipeline failed. Please check the logs for details.'
        }
    }
}