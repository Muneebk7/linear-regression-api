
pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Build and Deploy') {
            steps {
                checkout scm

                sh 'docker --version'
                sh 'docker-compose --version'
                sh 'docker-compose down || true'
                sh 'docker-compose up -d'
            }
        }
    }
}
