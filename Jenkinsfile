pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building project..."'
            }
        }
        
        stage('Test-master') {
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
