// //checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: '']])


// pipeline {
//     agent any

//     environment {
//         DOCKER_IMAGE_NAME = "deployment-master"
//         DOCKERHUB_CREDENTIALS_ID = "your-dockerhub-credentials-id"
//         REACT_APP_VERSION = "VERSION_REACT_1"
//         DOCKER_TAG = "master-tag"
//     }

//     stages {
//         stage('Pull Code from Git') {
//             steps {
//                 git branch: 'master', url: 'https://github.com/rishabhkhare314/jenkins-react-deployment.git'
//             }
//         }

// stage('Build Docker Image') {
//             steps {
//                 script {
//                     // Build Docker image with a build argument
//                     bat """
//                         docker build --build-arg REACT_APP_VERSION=${REACT_APP_VERSION} -t ${DOCKER_IMAGE_NAME}:${DOCKER_TAG} .
//                     """
//                 }
//             }
//         }
//         // stage('Install Dependencies') {
//         //     steps {
//         //         script {
//         //             // Installing dependencies
//         //             bat 'npm install'
//         //         }
//         //     }
//         // }

//         // stage('Build React App') {
//         //     steps {
//         //         script {
//         //             // Running the build command
//         //             bat 'npm run build'
//         //         }
//         //     }
//         // }
//     }
// }



pipeline {
    agent any
    stages {
        stage('PRINT VERSOINS') {
            steps {
                bat 'npm version'
            }
        }
    }
      stage('INSTALl DEPENDENCIES') {
            steps {
                bat 'npm run build'
            }
        }

}