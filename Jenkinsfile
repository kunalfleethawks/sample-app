#!/usr/bin/env groovy

pipeline {
    agent any

    options {
        buildDiscarder(logRotator(numToKeepStr: '10'))
        disableConcurrentBuilds()
        timeout(time: 1, unit: 'HOURS')
        timestamps() 
     }

 
    stages {
        stage('Build & Test') {
            steps{
                 nodejs(nodeJSInstallationName: 'nodejs12x') {
                    sh 'npm config ls'
                }
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

}
