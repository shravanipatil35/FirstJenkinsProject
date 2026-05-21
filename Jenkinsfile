pipeline {
    agent any

    stages {
        stage('Dev') {
            steps {
                echo 'I am in Development'
                echo 'checking git version'
                sh 'git --version'
            }
        }
        stage('Staging') {
            steps {
                echo 'I am in Staging'
                echo 'checking docker version'
                sh 'docker --version'
                sh 'docker pull nginx'
            }
        }
        stage('Production') {
            steps {
                echo 'I am in Production'
                echo 'listing docker images'
                sh 'docker images'
            }
        }
        stage('Container') {
            steps {
                echo 'I am in Container'
                echo 'Creating Container'
                sh 'docker run -d -p 80:80 nginx'
                echo 'container created'
            }
        }
    }
}
