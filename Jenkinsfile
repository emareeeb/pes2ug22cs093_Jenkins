pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Building C++ Project...'
                    sh 'g++ -o PES2UG22CS093-1 main.cpp'  
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    echo 'Running Tests...'
                    sh './PES2UG22CS093-1' 
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    sh './non_existing_file'  // Intentional error
                    echo 'Deploying the application...'
                    sh 'echo "Deployment successful!"'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed! Please check the logs for errors.'
        }
    }
}
