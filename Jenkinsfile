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
            withSonarQubeEnv('sonarserver') {
            sh "/home/bhupendra/sonarqube-10.3.0.82913/bin/sonar-scanner-4.7.0.2747-linux/bin/sonar-scanner -Dsonar.projectKey=testingpipeline"
            }
        }
     }



        }
}

