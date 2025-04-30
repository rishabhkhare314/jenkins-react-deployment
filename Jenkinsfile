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
        nodejs "NodeJS 18"
    }
    environment {
        secretToken = credentials("SECRET_TEXT")
    }

    stages {
        stage("NPM VERSION") {
            steps {
                echo 'npm version'
                bat 'npm version'
            }
        }
        stage("CHECKOUT") {
            steps {
                echo "CHECKOUT............."
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
 
}