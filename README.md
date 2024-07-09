# Jenkins Studies

[Doc. Jenkins](https://www.jenkins.io/doc/tutorials/)   

## Getting started with Jenkins - Download

[Doc.](https://www.jenkins.io/doc/pipeline/tour/getting-started/)

## Creating your first Pipeline 

[Hello World - Doc.](https://www.jenkins.io/doc/pipeline/tour/hello-world/)

````
Jenkinsfile (Declarative Pipeline)
/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'golang:1.22.5-alpine3.20' } }
    stages {
        stage('build') {
            steps {
                sh 'go version'
            }
        }
    }
}
````

## Configurando Nginx como Proxy Reverso 

[How To Configure Nginx as a Reverse Proxy for Jenkins](https://www.youtube.com/watch?v=yixMeJGtLFk)

