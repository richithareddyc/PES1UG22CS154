pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o YOUR_SRN-1 hello.cpp'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './YOUR_SRN-1'
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
