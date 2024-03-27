pipeline {
    agent any

    tools {nodejs "NodeJs"}
    stages {
        stage('Build') {
            steps {
                sh 'apt-get -s upgrade'
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'node ./app.js &'
            }
        }
    }
}
