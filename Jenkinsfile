pipeline {
    agent any
    stages {
        stage('run script') {
            sh "./run.sh"
        }
        stage('sleep 6 seconds') {
            sh "sleep 6"
        }
        stage('exit') {
            sh "exit"
        }
    }
}
