pipeline {
    agent {
        docker { image 'scm_image:1.0.2' }
    }

    stages {
        stage('Build') {
            steps {
                sh 'cat /etc/VERSION'
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