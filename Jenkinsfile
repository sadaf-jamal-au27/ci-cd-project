pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                echo "📥 Code checkout from GitHub"
                git branch: 'main',
                    url: 'https://github.com/sadaf-jamal-au27/ci-cd-project.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                echo "🐳 Building Docker image"
                sh 'docker build -t cicd-demo:latest .'
            }
        }

        stage('Run Container (Test)') {
            steps {
                echo "🚀 Running container for test"
                sh '''
                docker rm -f cicd-test || true
                docker run -d --name cicd-test -p 8086:80 cicd-demo:latest
                '''
            }
        }
    }

    post {
        success {
            echo "✅ Jenkins Pipeline SUCCESS"
        }
        failure {
            echo "❌ Jenkins Pipeline FAILED"
        }
    }
}
