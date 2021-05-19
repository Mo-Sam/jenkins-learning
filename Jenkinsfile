pipeline {
    agent { docker 
	{ 
		image 'python:3.5.1'
		args '-v C:\\Sarmad\\Learning\\Jenkins\\Pydocker:/user/sarmad'
	} }
    stages {
        stage('build') {
            steps {
                sh 'python --version'
            }
        }
	}
}
