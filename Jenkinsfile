//checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: '']])


pipeline {
    agent any

    environment {
        IMAGE_NAME = "your-docker-image-name"
        DOCKERHUB_CREDENTIALS_ID = "your-dockerhub-credentials-id"
    }

    stages {
        stage('Pull Code from Git') {
            steps {
                git branch: 'master', url: 'https://github.com/rishabhkhare314/jenkins-react-deployment.git'
            }
        }

    stage('Build Application') {
            steps {
                sh '''
                    # Example for a Node.js project
                    echo "Building the application..."
                    npm install
                    npm run build
                '''
                // For Java Maven project, it would be: mvn clean install
            }
        }
    }
}

