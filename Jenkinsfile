pipeline {
	agent any

	options {
		buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
		disableConcurrentBuilds()
	}
	stages {
		stage('Hello') {
			steps {
				echo "Hello Miao"
				echo "For Pull request only"
			}
		}

		stage ('cat README') {
		    when {
			    branch "feature*"
		    }
		    steps {
			sh '''
			    cat README.md
			'''
		    }
		}
	}

}
