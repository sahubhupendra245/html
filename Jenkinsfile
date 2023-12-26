pipeline {
    agent any

    stages {
        stage('Git checkout') {
            steps {
             script {   git branch: 'main', url: 'https://github.com/sahubhupendra245/html.git' }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
