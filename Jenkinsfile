pipeline {
    agent {
        docker { image 'scm_image:1.0.0' }
    }

    stages {
        stage('Container Verification') {
            steps {
                sh 'cat /etc/VERSION'
            }
        }
        stage('Build') {
            steps {
                sh 'mix deps.get'
                sh 'mix compile'
            }
        }
        stage('Test') {
            steps {
                sh 'mix test'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}