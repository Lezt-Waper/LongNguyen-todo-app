pipeline {
    agent any

    tools {nodejs "node"}
    stages {
        stage('Build') {
            steps {
                sh 'apt-get -s upgrade'
                sh 'apt-get -s install npm -y'
            }
        }
        stage('Test') {
            steps {
                sh 'node ./app.js'
            }
        }
    }
}
