pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building project..."'
            }
        }
        stage('Test') {
            steps {
                sh './hello.sh'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploying project..."'
            }
        }
    }
}
