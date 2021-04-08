// Scripted
// node {
// 		echo "Build"
// 		echo "Test"
// 		echo "Integration Test"
// }

// Declarative
pipeline {
	//agent any
	agent { Docker { image 'maven:3.6.3' } }
	stages {
		stage('Build') {
			steps {
				sh 'mvn --version'
				echo "Build"
			}
		}
		stage('Test') {
			steps {
				echo "Test"
			}
		}
		stage('Integration Test') {
			steps {
				echo "Integration Test"
			}
		}
	} 
	
	post {
		always {
			echo 'I m awesone, I run always'
		} 
		success {
			echo 'I run when you are successful'
		}
		failure {
			echo 'I run when you faile'
		}
	}
}