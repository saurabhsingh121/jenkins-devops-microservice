pipeline {
	// agent any
	// agent { docker { image 'maven:3.6.3'}}
	agent { docker { image 'node:latest'}}
	stages {
		stage("Build"){
			steps {
				// sh 'mvn --version'
				sh 'node --version'
				sh 'npm --version'
				echo "Build"
			}
		}
		stage("Test"){
			steps {
				echo "Test"
			}
		}
		stage("Integration Test"){
			steps {
				echo "Integration Test"
			}
		}
	}
	post {
		always {
			echo "I am awesome. I run always."
		}
		success {
			echo "I run when you are successful."
		}
		failure {
			echo "I run when you fail."
		}
		changed {
			echo "It runs when status of the build changes."
		}
	}
}