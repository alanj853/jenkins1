pipeline {
    agent any

    stages {
        stage('Container setup') {
            steps {
                echo 'Entering container...'
                withDockerContainer(image: 'scm_image:1.0.0') {
                  echo 'Confirming container...'
                  sh 'cat /etc/VERSION'  
                }
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
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