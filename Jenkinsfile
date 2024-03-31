pipeline {
    agent {
        docker {
            image 'node:16-alpine'
        }
    }

    stages {
        stage('Docker build') {
            agent any
            steps {
                sh 'docker build -t leztwaper/todo-app:5 .'
            }
        }
    }
}