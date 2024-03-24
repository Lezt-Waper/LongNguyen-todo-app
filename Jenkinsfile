pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'apt update'
                sh 'apt install npm -y'
            }
        }
        stage('Test') {
            steps {
                sh 'node ./app.js'
            }
        }
    }
}
