pipeline {
    agent any

    stages {
        stage('Pull from Git') {
            steps {
                git branch: 'main', url: 'https://github.com/CarolinaSFreitas/jenkins-studies.git'
            }
        }
        stage('Build in Docker') {
            agent {
                docker { image 'golang:1.22.5-alpine3.20' }
            }
            steps {
                sh 'go version'
            }
        }
    }
}
