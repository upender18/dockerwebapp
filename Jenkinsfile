
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
				sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u upender18 --password-stdin'
			}
		}

		stage('Push') {

			steps {
				sh 'docker push upender18/dockerwebapp:latest'
			}
		}
	}

	post {
		always {
			sh 'docker logout'
		}
	}

}
