pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                build 'PES1UG22CS362'
                sh 'g++ main.cpp -o PES1UG22CS362-1'
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22CS362-1'
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
