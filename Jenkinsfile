pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building C++ Project...'
                    sh 'g++ -o PES2UG22CS089_1 main.cpp'  
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running Tests...'
                    sh './PES2UG22CS089_1' 
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying the application...'
                    sh 'echo "Deployment successful!"'
                }
            }
        }
    post {
        failure {
            echo 'Pipeline failed! Please check the logs for errors.'
        }
    }
}
