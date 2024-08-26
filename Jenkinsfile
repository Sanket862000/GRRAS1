pipeline {
    agent any
    stages {
        stage ('chekout') {
            steps {
                chekout scm
            }
        }
        stage ('build') {
            steps {
                  sh '/home/sanket/Documents/devops/apache-tomcat-9.0.93/bin/mvn install'

            }
        }
        stage ('Deployment') {
            steps {
                sh 'target/GRRAS1.war /home/sanket/Documents/devops/apache-tomcat-9.0.93/webapps'
            }
        }
    }
}
