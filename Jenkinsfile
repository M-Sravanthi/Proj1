pipeline{

	agent any

	environment {
		DOCKERHUB_CREDENTIALS=credentials('dockerlogin')
	}
        stage('Login') {

			steps {
				sh 'echo $DOCKERHUB_CREDENTIALS_PSW | docker login -u $DOCKERHUB_CREDENTIALS_USR --password-stdin'
			}
		}

		stage('Push') {

			steps {
				sh 'docker push msravanthip/myapp'
			}
		}
	}
