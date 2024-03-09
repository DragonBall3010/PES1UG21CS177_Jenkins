pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                dir('main') {
                    sh 'g++ hello.cpp -o PES1UG21CS177'
                }
            }
        }
        stage('Test') {
            steps {
                dir('main') {
                    sh './PES1UG21CS177'
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
                sh 'this_command_give_an_error'
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
