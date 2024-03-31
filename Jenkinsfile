pipeline {
    agent none
    tools {docker 'docker'}

    stages {
        stage('Maven Install') {
            agent {
                docker {
                    image 'maven:lastest'
                }
            }
            steps {
                sh 'mvn clean install'
            }
        }

        stage('Docker build') {
            agent any
            steps {
                sh 'docker build -t leztwaper/todo-app:5 .'
            }
        }
    }
}