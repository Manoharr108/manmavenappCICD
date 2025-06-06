pipeline{
	agent any
	tools{
		maven 'maven'
	}
	stages{
		stage('Checkout'){
			steps{
				git "https://github.com/Manoharr108/manmavenappCICD"
			}
		}
		stage('Build'){
			steps{
				sh 'mvn clean install'
			}
		}
		stage('Deploy'){
			steps{
				sh 'sudo ansible-playbook ansible/deploy.yml  -i ansible/hosts.ini'
			}
		}
	}
}
		
