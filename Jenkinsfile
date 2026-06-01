pipeline {
    agent any

    tools {
        nodejs 'NodeJS18'
    }

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
<<<<<<< HEAD
                echo 'npm install'
=======
                sh 'node --version'
                sh 'npm --version'
                sh 'npm install'
>>>>>>> d0b625a (Added NodeJS tool configuration)
            }
        }

        stage('Test') {
            steps {
                echo 'npm test'
            }
        }
<<<<<<< HEAD

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
=======
>>>>>>> d0b625a (Added NodeJS tool configuration)
    }
}