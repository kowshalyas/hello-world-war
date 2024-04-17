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
                sh 'mvn clean package'
            }
        
        }
    }
}

    
