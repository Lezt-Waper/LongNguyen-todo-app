#!/usr/bin/env groovy

import groovy.transform.Field

@Field
String SSH_ID_REF = 'ssh-credentials-id'

pipeline {
    agent any
    tools {dockerTool 'docker'}

    stages {
        stage('Docker build') {
            steps {
                sh 'docker build -t vitnguyen/mgm-training-todo-app:0.0.3 .'
            }
        }

        stage('Push to DockerHub') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'v-docker-hub', usernameVariable: 'USER', passwordVariable: 'PASSWD')]) {
                    sh 'docker login -u "$USER" -p "$PASSWD"'
                    sh 'docker push vitnguyen/mgm-training-todo-app:0.0.3'
                }
            }
        }

        stage('Pull docker to EC2') {
            steps {
                withCredentials([sshUserPrivateKey(credentialsId: 'ssh-credentials-id', keyFileVariable: 'KEY')]) {
                    sh 'ssh -o "UserKnownHostsFile=/dev/null" -o "StrictHostKeyChecking=no" -i ${KEY} root@ec2-18-142-231-213.ap-southeast-1.compute.amazonaws.com docker ps'
                }
            }
        }
    }
}