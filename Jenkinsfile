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

    stages {
        stage("CHECKOUT") {
            steps {
                echo "CHECKOUT............."
            }
        }
        stage("INSTALL DEPENDENCIES") {
              steps {
                echo "INSTALL...DEPENDENCIES"
            }
        }
        stage("BUILD APP") {
              steps {
                echo "BUILD APPLICATIONS...."
              }
            }
        stage("GET SECRET CREDENTAILS") {
              steps {
                echo "ACCESS JENKINS SECRET"
              }
            }
        stage("RUN APPLICATION") {
              steps {
                 echo "RUN APPLCATIONS"
            }
        }
    }
 
}