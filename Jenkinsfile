pipeline {
    agent any

    parameters {
        choice(
            name: 'BRANCH_NAME',
            choices: ['main', 'master'],
            description: 'Select the branch to build from GitHub repo'
        )
    }

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM',
                    branches: [[name: "*/${params.BRANCH_NAME}"]],
                    doGenerateSubmoduleConfigurations: false,
                    extensions: [],
                    userRemoteConfigs: [[
                        url: 'https://github.com/Vikas0112/Very-Simple-Hell-World.git'
                    ]]
                ])
            }
        }

        stage('Build') {
            steps {
                sh 'echo "Building project..."'
            }
        }

        stage('Test') {
            steps {
                sh 'chmod +x hello-main.sh'
                sh './hello-main.sh'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo "Deploying project..."'
            }
        }
    }
}
