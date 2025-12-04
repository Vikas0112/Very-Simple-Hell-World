pipeline {
    agent any

    parameters {
        choice(
            name: 'BRANCH_NAME',
            choices: ['main', 'master'],
            description: 'Select which branch to build'
        )
    }

    hello
    stages {
        stage('Checkout') {
            steps {
                git branch: "${params.BRANCH_NAME}",
                    url: 'https://github.com/Vikas0112/Very-Simple-Hell-World.git'
            }
        }

        stage('Build') {
            steps {
                echo "Building project from ${params.BRANCH_NAME} branch..."
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
                echo "Deploying project from ${params.BRANCH_NAME} branch..."
            }
        }
    }
}
