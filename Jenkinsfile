pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                sh 'g++ -o output hell.cpp' // Compile the C++ file
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
                sh './output' // Run the compiled output file
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
