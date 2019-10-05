#!groovy


pipeline {
	agent any
	
	stages {
		stage('Build') {
			steps {
			
			echo "Building first job in Jenkins"
			}
		}
		
		stage('Test') {
				steps {
					echo "Hello World"
				}
		}

		stage('Deploy') {
			steps {
				script {
					echo "Deploying the job"
                	 sh "/usr/bin/aws s3 cp ./hello.py s3://teebucket1"
				}
			}
		}

	}

}