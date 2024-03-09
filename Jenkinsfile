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
            }
        }
    }
    post {
        failure {
            error 'Pipeline failed'
        }
    }
}
