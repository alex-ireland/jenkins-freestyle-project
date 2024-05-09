pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh "echo 'building...'"
                sh "pwd"
                sh "echo 'Hello World!' > code.sh"
            }
        }
        stage('test') {
            steps {
                sh "echo 'testing...'"
                sh "ls -la"
                script {
                    "RESULT=${(./code.sh)}"
                }
                script {
                    assert $RESULT == 'Hello World!'
                }
            }
        }
        stage('deploy') {
            steps {
                sh "echo 'deploying...'"
            }
        }
    }
}
