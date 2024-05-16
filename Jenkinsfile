
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
        stage('deploy') {
            steps {
                sh 'scp /home/slave9/workspace/pipeline_job2/target/hello-world-war-1.0.0.war root@172.31.17.156:/opt/apache-tomcat-8.5.100/webapps/'
            }
        
        }
        
    }
}
