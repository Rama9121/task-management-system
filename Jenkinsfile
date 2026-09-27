pipeline {

    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Checking source code...'
                checkout scm
            }
        }

        stage('Verify Jenkins') {
            steps {
                echo 'Jenkins is working'
                sh 'hostname'
                sh 'whoami'
            }
        }

        stage('Check Project') {
            steps {
                echo 'Checking repository files'
                sh 'ls -la'
            }
        }

    }

    post {

        success {
            echo 'Pipeline completed successfully'
        }

        failure {
            echo 'Pipeline failed'
        }

    }
}
