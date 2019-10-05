#!groovy


pipeline {
	agent any
	environment {
		export AWS_ACCESS_KEY_ID=aws_access_key_id
		export AWS_SECRET_ACCESS_KEY=aws_secret_access_key
		export AWS_DEFAULT_REGION=us-east-1
	}
	
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