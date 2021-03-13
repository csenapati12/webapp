pipeline {
    agent any   
    stages {
	    stage('Build and Package') {           	
            steps {
              withMaven {            
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
