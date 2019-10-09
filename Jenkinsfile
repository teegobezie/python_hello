#!groovy


pipeline {
	agent any
	
	stages {
		stage('Build') {
			steps {
			
			echo "Building the job"
			}
		}
		
		stage('Test') {
				steps {
					echo "Testing for the job"
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