pipeline {
    agent any   
    stages {
	    stage('Build and Package') {           	
            steps {
              withMaven(maven: 'maven-3.6.3') {           
		 script{
		    sh """
		mvn package
                """
		 }}
            }
        }
        stage('Ansible Deploy') {           	
            steps {
               script{              
                sh """
		  ansible --version
		  ansible-playbook deployfile.yml
                """
	       }
            }
        }
    }  
}
