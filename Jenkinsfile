pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh "echo 'building...'"
                sh "pwd"
                sh "echo 'echo Hello World!' > code.sh"
                sh "chmod a+x code.sh"
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
                    println RESULT
                    assert RESULT == "Hello World!"
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
