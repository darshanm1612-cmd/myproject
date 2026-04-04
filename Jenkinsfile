pipeline {
    agent any

    environment {
        IMAGE_NAME = "django-app"
        CONTAINER_NAME = "django-container"
    }

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/darshanm1612-cmd/myproject.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                bat "docker build -t %IMAGE_NAME% ."
            }
        }

        stage('Stop Old Container') {
            steps {
                bat "docker rm -f %CONTAINER_NAME% || exit 0"
            }
        }

        stage('Run Container') {
            steps {
                bat "docker run -d -p 8000:8000 --name %CONTAINER_NAME% %IMAGE_NAME%"
            }
        }
    }

    post {
        success {
            echo '✅ Deployment Successful!'
        }
        failure {
            echo '❌ Deployment Failed!'
        }
    }
}
