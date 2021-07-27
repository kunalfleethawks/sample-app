#!/usr/bin/env groovy

pipeline {
    agent any

    options {
        buildDiscarder(logRotator(numToKeepStr: '10'))
        disableConcurrentBuilds()
        timeout(time: 1, unit: 'HOURS')
        timestamps() 
     }

    tools {}

    environment {}

    stages {
        stage('Build & Test') {
            steps{
                sh("echo kunal")
            }
        }      

        stage('Build Docker Image') {
            steps{
            }
        
        }

        stage('Push Image to ECR') {
            steps{
            }
        
        }

        stage('Deploy in ECS') {
            steps{
            }
        }
    }

    post {}
}
