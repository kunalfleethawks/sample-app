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
                sh("echo kunal")
            }
        
        }

        stage('Push Image to ECR') {
            steps{
                sh("echo kunal")
            }
        }

        stage('Deploy in ECS') {
            steps{
                sh("echo kunal")
            }
        }
    }

    post {}
}
