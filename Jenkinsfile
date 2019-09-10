pipeline {
	agent any
	stages {
		stage('build') {
			step {
				sh 'mvn clean package'
			}

		}
		stage('test'){
			step {
				sh 'mvn test' 
			}
			post {
				always{

					junit 'target/surefire-reports/*.xml'
				}
			}

		}
	}
}