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
                    docker.image('fastapi-app').run('-p 8771:8000').start()
                }
            }
            post {
                success {
                    script {
                        echo 'FastAPI application is running on http://<your-server-ip>:8000'
                    }
                }
            }
        }
    }
}
