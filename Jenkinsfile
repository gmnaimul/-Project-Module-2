pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'git@github.com:gmnaimul/-Project-Module-2.git',
                    credentialsId: 'github-ssh'
            }
        }

        stage('Read hello.txt') {
            steps {
                script {
                    def content = readFile 'hello.txt'
                    echo "Contents of hello.txt:\n${content}"
                }
            }
        }
    }
}
