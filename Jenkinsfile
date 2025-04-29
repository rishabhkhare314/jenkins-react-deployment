pipeline {
    agent any

    environment {
        secret = credentials('SECRET_TEXT')
    }

    stages {
        stage("VERSIONS") {
            steps{
                echo "SHOW VERSIONS............."
                echo "SECRET:::::::::::::::::::::$secret"
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