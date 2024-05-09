pipeline {
    agent any
    stages {
        stage('run script') {
            sh "./run.sh"
        }
        stage('sleep 5 seconds') {
            sh "sleep 5"
        }
        stage('exit') {
            sh "exit"
        }
    }
}