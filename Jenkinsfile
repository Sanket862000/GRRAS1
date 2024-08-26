pipeline {
    agent any
    stages {
        stage ('chekout') {
            steps {
              git 'https://github.com/Sanket862000/REDHAT.git'   
            }
        }
        stage ('build') {
            steps {
                  sh 'mvn install'

            }
        }
        stage ('Deployment') {
            steps {
                sh 'cp target/GRRAS1.war /home/sanket/Documents/devops/apache-tomcat-9.0.93/webapps'
            }
        }
    }
}
