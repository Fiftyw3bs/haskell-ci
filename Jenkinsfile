pipeline {
    environment {
        HOME = '.'
    }
    agent {
        docker { image 'inputoutput/plutus-starter-devcontainer:latest' }
    }
    stages {
        stage('Prepare') {
            steps { sh 'cd /home/code/plutus-apps && nix-shell && cd /home/code/DAgriBiz/blockchain' }
        }

        stage('Build') {
            steps { sh 'cabal build dagribiz-pab' }
        }
    }
}
