pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'apt-get update'
                sh 'apt-get install npm -y'
            }
        }
        stage('Test') {
            steps {
                sh 'node ./app.js'
            }
        }
    }
}
