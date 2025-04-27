//checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: '']])


pipeline {
    agent any

    // environment {
    //     IMAGE_NAME = "your-docker-image-name"
    //     DOCKERHUB_CREDENTIALS_ID = "your-dockerhub-credentials-id"
    // }

    stages {
        stage('Pull Code from Git') {
            steps {
                git branch: 'master', url: 'https://github.com/rishabhkhare314/jenkins-react-deployment.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    // Installing dependencies
                    sh 'npm install'
                }
            }
        }

        stage('Build React App') {
            steps {
                script {
                    // Running the build command
                    sh 'npm run build'
                }
            }
        }
    }
}

