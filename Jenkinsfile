pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                checkout scm
            }
        }
        stage('Install Python') {
            steps {
                sh '''
                apt-get update
                apt-get install -y python3
                '''
            }
        }


        stage('Build') {
            steps {
                echo 'Building the application...'
                sh 'python3 test.py'
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests...'
                
            }
        }
    }
    post {
        always {
            echo 'Pipeline Project webhook python'
        }
    }
}
