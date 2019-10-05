#!groovy


pipeline {
	agent any
	
	stages {
		stage('Build') {
			steps {
			
			sh 'echo "Building first job in Jenkins"'
			}
		}
		
		stage('Test') {
				steps {
					sh 'echo "Hello World"'
				}
		}

		stage('Deploy') {
			steps {
				sh 'echo "Deploying the job"'
                sh 'aws s3 cp ./hello.py s3://teebucket1
			}
		}

	}

}