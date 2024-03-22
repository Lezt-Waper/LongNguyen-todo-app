pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'sudo npm install'
                sh 'node ./app.js'
            }
        }
    }
}
