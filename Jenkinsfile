
pipeline{

	agent any



	stages {

		stage('Build') {

			steps {
				sh 'docker build -t upender18/dockerwebapp:latest .'
			}
		}

		stage('Login') {
			steps {
				sh 'docker login -u upender18 -p Ofeb@098498 --password-stdin'
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
