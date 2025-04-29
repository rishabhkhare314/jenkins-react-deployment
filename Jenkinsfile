pipeline {
    agent any

    stages {
        stage("VERSIONS") {
            steps{
                echo "SHOW VERSIONS............."
                echo "SECRET:::::::::::::::::::::$SECRET_TEXT"
                bat "npm version"
            }
          
        }

        stage("INSTALL DEPENDENCIES") {
            steps {
                echo "SHOW VERSIONS............."
                bat "npm install"
        }
        }

        stage("REACT BUILD") {
            steps {
                echo "SHOW VERSIONS............."
                bat "npm run build"
            }
          
        }
    }
}