pipeline {
    agent { docker 
	{ 
		image 'python:3.5.1'
	} }
    stages {
        stage('build') {
            steps 
			{
				timeout(time:10, unit: 'SECONDS')
				{
					sh 'sleep 30'
				}
            }
        }
	}
	post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}