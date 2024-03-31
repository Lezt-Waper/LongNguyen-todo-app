pipeline {
    agent {
        docker {
            image 'maven:lastest'
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