pipeline {
    agent any   
    stages {
	    stage('Build and Package') {           	
            steps {
              // withMaven {            
		 scripts{
		    sh """
		mvn package
                """
	       }
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
