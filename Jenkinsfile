pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o PES1UG22AM054-1 main1.cpp' // Replace `YOUR_SRN` with your ID
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './PES1UG22AM054-1' // Run the compiled executable
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    echo 'Deploying application...'
                }
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
