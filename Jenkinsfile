pipeline{
	agent any
	tools{
		maven 'Maven'
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
				sh 'sudo ansible-playbook ansible/playbook.yml  -i ansible/hosts.ini'
			}
		}
	}
}
		
