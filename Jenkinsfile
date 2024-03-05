pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    Build 'PES1UG21CS210-1'
                    sh 'g++ main.cpp -o output' 
                }
                echo 'Build Stage Successful'
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './output'
                }
                echo 'Test Stage Successful'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploy'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
