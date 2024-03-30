pipeline {
    agent any

    tools {docker "docker"}
    stages {
        stage('Build') {
            steps {
                sh 'docker build -t leztwaper/todo-app:5 .'
            }
        }
        stage('Test') {
            steps {
                sh 'echo Test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Deploy'
            }
        }
    }
}
