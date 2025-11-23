pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/prakhar5100/jenkins-repo.git'            }
        }

        stage('Build') {
            steps {
                echo "Building the project..."
            }
        }

        stage('Test') {
            steps {
                echo "Testing the project..."
            }
        }

        stage('Archive Artifact') {
            steps {
                sh 'echo "This is the build artifact" > output.txt'
                archiveArtifacts artifacts: 'output.txt', fingerprint: true
            }
        }
    }
}
