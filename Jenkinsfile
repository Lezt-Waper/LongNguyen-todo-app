pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'apt update'
                sh 'apt install npm'
            }
        }
        stage('Test') {
            steps {
                sh 'node ./app.js'
            }
        }
    }
}
