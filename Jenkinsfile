pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git 'https://github.com/Aarav2411/myci-cd.git'
            }
        }

        stage('Install') {
            steps {
                sh 'npm install'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Code Check') {
            steps {
                sh 'npm audit || true'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Package') {
            steps {
                sh 'tar -czf app.tar.gz *'
            }
        }
    }
}
