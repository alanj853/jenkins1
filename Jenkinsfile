pipeline {
    agent {
        docker { image 'scm_image:1.0.0' }
    }

    stages {
        stage('Build') {
            steps {
                sh 'VERSION=$(cat /etc/VERSION)'
                sh 'echo "Building with $VERSION"'
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