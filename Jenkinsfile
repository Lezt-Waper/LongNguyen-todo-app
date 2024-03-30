pipeline {
    agent any

    tools {docker "Docker"}
    stages {
        stage('Build') {
            app = docker.build("leztwaper-todo-app:5")
        }
        stage('Test') {
            app.inside {
                sh 'echo "Test"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo Deploy'
            }
        }
    }
}
