pipeline{

	agent any

	environment {
		DOCKERHUB_CREDENTIALS=credentials('priscillajb-dockerhub')
	}

	stages {
	    
	    stage('gitclone') {

			steps {
				git 'https://github.com/PriscillaJB19/Node.git'
			}
		}

		stage('Build') {

			steps {
				sh 'docker build -t priscillajb/node-app:1.0'
			}
		}

		stage('Login') {

			steps {
				sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
			}
		}

		stage('Push') {

			steps {
				sh 'docker push priscillajb/node-app:1.0'
			}
		}
	}

}
