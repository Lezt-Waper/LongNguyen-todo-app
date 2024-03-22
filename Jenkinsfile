pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                sh 'ls -la'
                sh 'npm install'
                sh 'node app.js'
            }
        }
    }
}
