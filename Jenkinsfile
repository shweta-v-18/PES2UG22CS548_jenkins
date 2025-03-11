pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o hello hello.cpp' // Compile C++ file
            }
        }
        stage('Test') {
            steps {
                sh './hello' // Run the compiled output
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline Failed'
        }
    }
}
