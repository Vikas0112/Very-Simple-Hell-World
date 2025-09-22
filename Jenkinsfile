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
        sh 'chmod +x hello-master.sh'
        sh './hello-master.sh'
    }
}

        stage('Deploy') {
            steps {
                sh 'echo "Deploying project..."'
            }
        }
    }
}
