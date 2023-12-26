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
             echo "testing has sepatate job"
            }
        }

                stage('Creating Docker Image') {
            steps {
                withCredentials([string(credentialsId: 'dockerlogin', variable: 'dtoken')]) {
                sh 'docker --version'
                sh 'docker login -u bhupendra8888 -p $dtoken'
                sh 'docker logout'
                }
             

            }
        }


     }



        }

