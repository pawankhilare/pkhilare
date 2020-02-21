#!/usr/bin/env groovy

pipeline {

    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh "accept.sh"
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                
            }
        }
    }
}
