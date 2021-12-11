pipeline {
    environment {
        HOME = '.'
    }
    agent {
        docker { image 'inputoutput/plutus-starter-devcontainer:latest' }
    }
    stages {
        stage('Install') {
            steps { sh 'cabal update && cabal install --only-dependencies --enable-tests && cabal configure --enable-tests' }
        }
        stage('Build') {
            steps { sh 'cabal build main-is' }
        }
    }
}
