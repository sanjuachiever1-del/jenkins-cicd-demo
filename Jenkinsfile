pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t jenkins-cicd-demo .'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                docker stop demo-container || true
                docker rm demo-container || true

                docker run -d \
                --name demo-container \
                -p 3000:3000 \
                jenkins-cicd-demo
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully'
        }

        failure {
            echo 'Pipeline failed'
        }
    }
}
