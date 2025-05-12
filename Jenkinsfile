pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/Syogini1983/inventory-app-devops-demo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                // Add test steps if available, else echo
                echo 'Running tests (simulated)...'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t technova-inventory-app .'
            }
        }

        stage('Deploy with Docker') {
            steps {
                sh 'docker run -d -p 8080:8080 technova-inventory-app'
            }
        }
    }
}

