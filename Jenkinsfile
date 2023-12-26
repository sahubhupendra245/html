pipeline {
    agent any

    stages {

        stage('Git checkout') {
            steps {
             git branch: 'main', url: 'https://github.com/sahubhupendra245/html.git'
            }
        }


     stage('SonarQube Analysis') {
            def scannerHome = tool 'localsonarserver';
            withSonarQubeEnv() {
            sh "${scannerHome}/bin/sonar-scanner"
            }
     }


        
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
