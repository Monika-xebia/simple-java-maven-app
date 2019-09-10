pipeline {
	agent any
	stages {
		stage('build') {
			step {
				mvn clean package
			}

		}
		stage('test'){
			step {
				mvn test 
			}
			post {
				always{
					
					junit 'target/surefire-reports/*.xml'
				}
			}

		}
	}
}