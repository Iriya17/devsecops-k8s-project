pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                echo "Code pulled from GitHub"
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t myapp .'
            }
        }

        stage('Run Trivy Scan') {
            steps {
                sh 'trivy image myapp'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deployment will be handled later by Kubernetes"
            }
        }
    }
}
