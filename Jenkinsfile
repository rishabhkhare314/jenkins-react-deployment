// pipeline {
//     agent any

//     environment {
//         secret = credentials('SECRET_TEXT')
//     }

//     stages {
//         stage("VERSIONS") {
//             steps{
//                 echo "SHOW VERSIONS............."
//                 echo "SECRET:::::::::::::::::::::$secret"
//                 bat "npm version"
//             }
          
//         }

//         stage("INSTALL DEPENDENCIES") {
//             steps {
//                 echo "SHOW VERSIONS............."
//                 bat "npm install"
//         }
//         }

//         stage("REACT BUILD") {
//             steps {
//                 echo "SHOW VERSIONS............."
//                 bat "npm run build"
//             }
          
//         }
//     }
// }



































pipeline {
    agent any

    tools {
        nodejs "NODEJS-18"
    }
    environment {
        secretToken = credentials("SECRET_TEXT")
        DOCKER_IMAGE = "react-app-image"
        DOKCER_TAG = "latest"
    }

    stages {
        stage("NPM VERSION") {
            steps {
                echo 'npm version'
                bat 'npm version'
            }
        }

        stage("CHECKOCUT") {
            steps {
                echo "CHECKOUT CODE FDROM GIT REPOSITORY"
                checkout scm
            }
        }
       stage("BUILD DOckER IMAGE") {
        steps {
                        docker.build("DOCKER_IMAGE}:${DOKCER_TAG}")

        }
       }
       stage("RUN DOCKER CONAINER") {
        steps {
            docker.image("${DOCKER_IMAGE}:${DOCKER_TAG}").run('-d -p 3000:3000')
        }

       }
        stage("INSTALL DEPENDENCIES") {
              steps {
                echo "INSTALL...DEPENDENCIES"
                bat 'npm install'
            }
        }
        stage("BUILD APP") {
              steps {
                echo "BUILD APPLICATIONS...."
                bat 'npm run build'
              }
            }
        stage("GET SECRET CREDENTAILS") {
              steps {
                echo "ACCESS JENKINS SECRET $secretToken ......." 
              }
            }
        stage("RUN APPLICATION") {
              steps {
                 echo "RUN APPLCATIONS"
                 
            }
        }
        }

        post {
            success {
                echo "Pipeline completed successfully"
            }
            failure {
                echo "Pipeline failed.........."
            }
            always {
                echo "Pipeline always runs"
            }
    }
 
}