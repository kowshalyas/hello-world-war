
pipeline {
    agent any
    stages {
        stage('clone') {
            steps {
                sh 'rm -rf hello-world-war '
                sh 'git clone https://github.com/kowshalyas/hello-world-war.git'
            }
        
        }
        stage('build') {
            steps {
                sh 'docker build -t kowshi226/kowshalya:1.0.1 .'
            }
        
        }
       
