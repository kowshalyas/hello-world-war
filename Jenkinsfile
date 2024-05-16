
pipeline {
    agent any
        stages {
        stage('checkout') {
            steps {
                sh 'rm -rf hello-world-war'
                sh 'git clone https://github.com/lalithav23/hello-world-war.git'
            }
        }
         stage('build') {
            steps {
                sh "docker build -t lalithav23/hello-world-war:1.0.1 ."
            }
        }
       stage('publish') {
            steps {
                withCredentials([usernamePassword(credentialsId: '6dfee5c1-391d-4c2f-8a91-d784f0dca5ec', usernameVariable: 'DOCKER_USERNAME', passwordVariable: 'DOCKER_PASSWORD')]) {
                    sh "docker login -u ${DOCKER_USERNAME} -p ${DOCKER_PASSWORD}"
                    sh "docker push kowshi226/kowshalya:1.0.1"
                }
            }
        }     
    }
}
