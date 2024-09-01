pipeline {
	agent{
	label 'slave-label'
	}
	stages {
	    stage('Checkout') {
	        steps {
			checkout scm			       
		      }}
		stage('Build') {
	           steps {
			  sh 'JAVA_HOME=/home/sanket/slaves/jdk-11.0.24 /home/sanket/slaves/apache-maven-3.9.8/bin/mvn install'
	                 }}
		stage('Deployment'){
		    steps {
			sh 'cp target/GRRAS1.war /home/sanket/slaves/apache-tomcat-9.0.93/webapps'
			}}	
}}
