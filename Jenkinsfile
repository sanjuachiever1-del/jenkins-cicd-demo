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
                echo 'npm install'
            }
        }

        stage('Test') {
            steps {
                echo 'npm test'
            }
        }

        stage('Docker Build') {
            steps {
                echo 'docker build -t jenkins-cicd-demo .'
            }
        }

        stage('Deploy') {
            steps {
                echo 'docker run -d -p 3000:3000 jenkins-cicd-demo'
            }
        }
    }
}
