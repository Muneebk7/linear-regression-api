
pipeline {
    agent any

    triggers {
        githubPush()
    }

    stages {
        stage('Build and Deploy') {
            steps {
                checkout scm
                sh 'docker-compose down || true'
                sh 'docker-compose up -d'
            }
        }
    }
}
