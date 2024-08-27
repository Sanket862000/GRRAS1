pipeline {
    agent any
    parameters {
  choice choices: ['DEV', 'QA', 'UAT'], description: 'this choice parameter', name: 'ENVIRONMENT'
}
    triggers {
  pollSCM '* * * * *'
}
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
                script {
                    if [ env.ENVIRONMENT = "QA" ];then
         sh 'cp target/GRRAS1.war /home/sanket/Documents/Devops/apache-tomcat-9.0.93/webapps'
	elif  [ env.ENVIRONMENT = "UAT" ];then
         sh'cp target/GRRAS1.war /home/swapnil/Documents/DevOps-Software/apache-tomcat-9.0.79/webapps'
echo "deployment has been done!"
fi

                }
            }
        }
    }
}
