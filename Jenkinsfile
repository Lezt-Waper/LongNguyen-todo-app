node {
    
    stage('Build') 
    def app = docker.build 'leztwaper/todo-app:5'
    
    stage('Test') 
    app.inside {
        sh 'echo test'
    }
    
    stage('Deploy') 
    sh 'echo Deploy'
}
