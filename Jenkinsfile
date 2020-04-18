pipeline {
    env.DOCKER_IMAGE='scm_image:1.0.0'
    agent {
        docker { image ${DOCKER_IMAGE} }
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