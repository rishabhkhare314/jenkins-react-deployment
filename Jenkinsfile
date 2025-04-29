pipeline {
    agent any

    tools {
        nodejs '20.4.2'
    }

    stages {
        stage("VERSIONS") {
            steps{
                echo "SHOW VERSIONS............."
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