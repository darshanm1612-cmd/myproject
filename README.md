# myproject
# 🚀 Django CI/CD Project

## 📌 Description
This project is a Django web application deployed using Docker and automated using Jenkins CI/CD pipeline.

## ⚙️ Technologies Used
- Python
- Django
- Docker
- Jenkins
- GitHub

## ▶️ How to Run

### Run Locally
python manage.py runserver

Open:
http://127.0.0.1:8000

### Run with Docker
docker build -t django-app .
docker run -d -p 8001:8000 django-app

Open:
http://localhost:8001

## 📸 Screenshots

### Application (Local)
![App Local](screenshots/app-local-8000.png)

### Application (Docker)
![App Docker](screenshots/app-docker-8001.png)

### Admin Dashboard
![Admin](screenshots/admin-dashboard.png)

### Jenkins Pipeline
![Jenkins](screenshots/jenkins-pipeline-success.png)

### Jenkins Console
![Console](screenshots/jenkins-console-output.png)
