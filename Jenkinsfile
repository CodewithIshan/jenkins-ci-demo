pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/CodewithIshan/jenkins-ci-demo.git'
'
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
        stage('Test') {
            steps {
                sh 'npm test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying application...'
                // Example: copy files to a deploy directory
                sh 'mkdir -p deploy && cp -r * deploy/'
            }
        }
    }
}