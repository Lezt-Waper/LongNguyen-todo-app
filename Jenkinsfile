#!/usr/bin/env groovy

import groovy.transform.Field

@Field
String DOCKER_USER_REF = '<DOCKERHUB_ID_PLACEHOLDER>'
@Field
String SSH_ID_REF = '<SSH_ID_PLACEHOLDER>'

pipeline {
    agent any
    tools {dockerTool 'docker'}

    stages {
        stage('Docker build') {
            steps {
                sh 'docker build -t vitnguyen/mgm-training-todo-app .'
            }
        }

        stage('Push to DockerHub') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'v-docker-hub', usernameVariable: 'USER', passwordVariable: 'PWD')]) {
                    sh 'docker login -u "$USER" -p "$PWD"'
                    sh 'docker push vitnguyen/mgm-training-todo-app'
                }
            }
        }
    }
}