pipeline {
    agent any

    stages {
        stage('Checkout Verification') {
            steps {
                echo 'GitHub repository connected!'
                sh 'pwd'
                sh 'ls -la'
            }
        }

        stage('Build') {
            steps {
                echo 'Starting application build...'
                sh 'docker build -t jenkins-demo:v1 -f docker/Dockerfile .'
            }
        }

        stage('Success') {
            steps {
                echo 'Docker image build completed!'
            }
        }
    }
}
