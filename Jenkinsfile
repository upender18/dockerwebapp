
pipeline{

	agent any

	environment {
		DOCKERHUB_CREDENTIALS=credentials('dockerHub')
	}

	stages {

		stage('Build') {

			steps {
				sh 'docker build -t upender18/dockerwebapp:latest .'
			}
		}

		stage('Login') {

			steps {
				sh 'sudo docker login -u upender18 -p Ofeb@098498'
			}
		}

		stage('Push') {

			steps {
				sh 'sudo docker push upender18/dockerwebapp:latest'
			}
		}
	}

	post {
		always {
			sh 'sudo docker logout'
		}
	}

}
