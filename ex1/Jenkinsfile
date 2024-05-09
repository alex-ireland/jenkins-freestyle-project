pipeline {
    agent any
    stages {
        stage('run script') {
            steps {
                sh "./run.sh"
            }
        }
        stage('sleep 4 seconds') {
            steps {
                sh "sleep 4"
            }
        }
        stage('exit') {
            steps {
                sh "exit"
            }
        }
    }
}
