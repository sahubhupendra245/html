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
                sh 'docker image build -t bhupendra8888/webapp:latest .'
                sh 'docker login -u bhupendra8888 -p $dtoken && \
                docker push bhupendra8888/webapp:latest && \
                docker logout'
                }
    

            }
        }


            stage('Deploy image in development namespace') {
                 steps {
                 sh 'ssh -i /opt/mads_kubernetes mads@192.168.1.100 kubectl apply -f /home/mads/edureka-project/edureka-development.yaml'
            }
        }


     }



        }

