pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'ls -l'
                sh 'cd main && g++ PES1UG22CS622.cpp -o PES1UG22CS622'
            }
        }

        stage('Test') {
            steps {
                sh 'cd main && ./PES1UG22CS622'
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
