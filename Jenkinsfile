pipeline {
    environment {
        HOME = '.'
    }
    agent {
        docker { image 'inputoutput/plutus-starter-devcontainer:latest' }
    }
    stages {
        stage('Build') {
            steps { sh 'cabal build dagribiz-pab' }
        }
    }
}
