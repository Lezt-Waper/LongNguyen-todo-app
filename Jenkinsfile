pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'apt-get upgrade'
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
