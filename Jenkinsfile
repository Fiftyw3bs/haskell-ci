pipeline {
    environment {
        HOME = '.'
    }
    agent {
        docker { image 'nixos/nix:latest' }
    }
    stages {
        stage('Build') {
            steps { sh 'cabal build dagribiz-pab' }
        }
    }
}
