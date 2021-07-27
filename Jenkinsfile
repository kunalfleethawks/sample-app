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
                    sh 'npm install && node --version'                   
                }
            }
        }      

        stage('Build Docker Image using Code Build') {
            steps{
                awsCodebuild credentialsId: 'was-code-build-grovvy', credentialsType: 'jenkins', downloadArtifacts: 'false', projectName: 'new-jenkins-project', region: 'ap-south-1', sourceControlType: 'jenkins'
            }
        
        }
        
        stage('Deploy in ECS') {
            steps{
                sh("echo kunal")
            }
        }
    }

}
