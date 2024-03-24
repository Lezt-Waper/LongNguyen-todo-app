pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'sudo apt-get upgrade'
                sh 'sudo apt-get install npm -y'
            }
        }
        stage('Test') {
            steps {
                sh 'node ./app.js'
            }
        }
    }
}
