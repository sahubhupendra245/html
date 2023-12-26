pipeline {
    agent any

    stages {

        stage('Git checkout') {
            steps {
             git branch: 'main', url: 'https://github.com/sahubhupendra245/html.git'
            }
        }


        stage('SonarQube Analysis') {
            steps {
            def scannerHome = tool 'sonarserver';
            withSonarQubeEnv() {
            sh "${scannerHome}/bin/sonar-scanner"
            }
        }
     }



        }
}

