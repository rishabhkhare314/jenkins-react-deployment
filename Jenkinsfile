pipeline {
    agent any

    tools {
        nodejs '20.4.2'
    }

    stages {
        stage("VERSIONS") {
            step{
                echo "SHOW VERSIONS............."
                bat "npm version"
            }
          
        }

        stage("INSTALL DEPENDENCIES") {
            step {
                echo "SHOW VERSIONS............."
                bat "npm install"
        }
        }

        stage("REACT BUILD") {
            step {
                echo "SHOW VERSIONS............."
                bat "npm run build"
            }
          
        }
    }
}