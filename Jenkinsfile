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
                    sh 'docker stop fastapi-app-container || true'
                    sh 'docker rm fastapi-app-container || true'
                    docker.image('fastapi-app').run('--name fastapi-app-container -p 8775:8000')
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
