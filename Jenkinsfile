pipeline {
    agent any

    stages {
        stage('Checkout - master') {
            steps {
                checkout([$class: 'GitSCM',
                    branches: [[name: '*/master']],
                    userRemoteConfigs: [[
                        url: 'https://github.com/Vikas0112/Very-Simple-Hell-World.git'
                    ]]
                ])
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Building project from MASTER branch..."'
            }
        }

        stage('Test') {
            steps {
                sh 'chmod +x hello.sh'
                sh './hello.sh'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying project from MASTER branch..."'
            }
        }
    }
}
