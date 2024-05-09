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
                    RESULT = sh (
                        script: './code.sh',
                        returnStdout: true
                    ).trim()
                }
                // sh "RESULT="$(./code.sh)""
                echo $RESULT
                // script {
                //     assert $RESULT == 'Hello World!'
                // }
            }
        }
        stage('deploy') {
            steps {
                sh "echo 'deploying...'"
            }
        }
    }
}
