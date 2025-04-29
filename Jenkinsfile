pipeline {
    agent any

    tools {
        nodejs '20.4.2'
    }

    steps {
        step("VERSIONS") {
            echo "SHOW VERSIONS............."
            bat "npm version"
        }

        step("INSTALL DEPENDENCIES") {
            echo "SHOW VERSIONS............."
            bat "npm install"
        }

        step("REACT BUILD") {
           echo "SHOW VERSIONS............."
            bat "npm run build"
        }
    }
}