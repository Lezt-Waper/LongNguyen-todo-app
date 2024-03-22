pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'sudo npm install -g'
                sh 'node ./app.js'
            }
        }
    }
}
