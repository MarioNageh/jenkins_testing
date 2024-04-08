pipeline {
    agent any
    stages {
        stage('Build Docker Image') {
            steps {
                script {
                    docker.build('fastapi-app', '.')
                }
            }
        }
        stage('Run FastAPI Application') {
            steps {
                script {
                    docker.image('fastapi-app').run('-p 8775:8000')
                }
            }
            post {
                success {
                    script {
                        echo 'FastAPI application is running on http://<your-server-ip>:8775'
                    }
                }
            }
        }
    }
}