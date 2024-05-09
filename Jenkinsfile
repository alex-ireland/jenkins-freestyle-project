pipeline {
    agent any
    stages {
        stage('run script') {
            steps {
                sh "./run.sh"
            }
        }
        stage('sleep 6 seconds') {
            steps {
                sh "sleep 6"
            }
        }
        stage('exit') {
            steps {
                sh "exit"
            }
        }
    }
}
