pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building project..."'
            }
        }
        
        stage('Test-main') {
    steps {
        sh 'chmod +x hello.sh'
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
