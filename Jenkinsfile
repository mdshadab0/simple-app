pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/YOUR_USERNAME/simple-app.git'
            }
        }

        stage('Build') {
            steps {
                sh 'docker build -t simple-node-app .'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing... (this can be expanded)'
            }
        }

        stage('Deploy') {
            steps {
                sh 'docker run -d -p 3000:3000 --name nodeapp simple-node-app'
            }
        }
    }
}

