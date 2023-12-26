pipeline {
    agent any
    environment {
        dtoken    = credentials('DOTOKEN')
        
    }
    stages {

        stage('Git checkout') {
            steps {
             git branch: 'main', url: 'https://github.com/sahubhupendra245/html.git'
            }
        }


        stage('SonarQube Analysis') {
            steps {
             echo "testing has sepatate job"
            }
        }

                stage('Creating Docker Image') {
            steps {
             sh 'docker --version'
            }
        }


     }



        }

