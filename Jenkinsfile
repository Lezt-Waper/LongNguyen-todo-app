pipeline {
    agent any
    tools {dockerTool 'docker'}

    stages {
        stage('Docker build') {
            agent any
            steps {
                sh 'docker build -t leztwaper/todo-app:5 .'
            }
        }
    }
}