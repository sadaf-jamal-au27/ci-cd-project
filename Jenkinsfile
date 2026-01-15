pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/sadaf-jamal-au27/ci-cd-project.git'
            }
        }

        stage('Docker Build') {
            steps {
                sh '''
                  docker --version
                  docker build -t cicd-demo:latest .
                '''
            }
        }
    }
}
