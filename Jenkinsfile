pipeline {
    agent any

    stages {

        stage('Git checkout') {
            steps {
             git branch: 'main', url: 'https://github.com/sahubhupendra245/html.git'
            }
        }


     stages('SonarQube Analysis') {
            sonar.projectKey=testingpipeline
     }


        
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
