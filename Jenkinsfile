pipeline {
    agent any

    tools {
        nodejs '20.4.2'
    }

    steps {
        step("VERSIONS") {
            bat "npm version"
        }

        step("INSTALL DEPENDENCIES") {
            bat "npm install"
        }

        step("REACT BUILD") {
            bat "npm run build"
        }
    }
}