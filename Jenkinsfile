pipeline {
    agent docker-agent
    trigger {
        githubpush()
    }
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code...'
                checkout scm
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
            
        }t 
    }
}

