pipeline {
    tool {Docker 'Docker'}

    stages {
        stage('Build') {
            steps {
                docker build -t leztwaper/todo-app:5 .
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
