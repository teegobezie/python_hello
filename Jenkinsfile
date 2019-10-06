#!groovy


pipeline {
	agent any
	environment {
		aws_access_key_id="$AWS_ACCESS_KEY_ID"
		aws_secret_access_key="$AWS_SECRET_ACCESS_KEY"
		aws_default_region="$AWS_DEFAULT_REGION"
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