node {
    tool {Docker "Docker"}
    def app

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
