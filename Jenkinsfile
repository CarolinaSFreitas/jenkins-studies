pipeline {
    agent any

    stages {
        stage('Pull from Git') {
            steps {
                git branch: 'main', url: 'https://github.com/CarolinaSFreitas/jenkins-studies.git'
            }
        }
        stage('Docker Debug') {
            steps {
                script {
                    // Verifica se o Docker está funcionando
                    sh 'docker --version'
                    sh 'docker ps'
                }
            }
        }
        stage('Build in Docker') {
            agent {
                docker { image 'golang:1.20.5-alpine3.18' }
            }
            steps {
                sh 'go version'
            }
        }
    }
}
