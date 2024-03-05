pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                    build 'PES1UG21CS210-1'
                    sh 'g++ main.cpp -o output' 
            }
        }

        stage('Test') {
            steps {
                    sh 'some_non_existent_command'
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
