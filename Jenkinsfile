pipeline {
    environment {
        HOME = '.'
    }
    agent {
        docker { image 'nixos/nix:latest' }
    }
    stages {
        stage('Install') {
            steps { sh 'cabal update && cabal install --only-dependencies --disable-tests && cabal configure' }
        }
        stage('Build') {
            steps { sh 'cabal build main-is ' }
        }
    }
}
