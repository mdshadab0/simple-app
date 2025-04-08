pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git credentialsId: 'f721d32e-1533-4976-9f2b-bfa373352a84', url: 'https://github.com/mdshadab0/simple-app.git'

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

