pipeline{
	agent {label 'slave'}
	stages{
		stage('Clone repo'){
			steps{
				git 'https://github.com/jglick/simple-maven-project-with-tests'
			}
		}
		stage('Build project'){
			steps{
				
				sh 'mvn -B -ntp -Dmaven.test.failure.ignore verify'
			}

		}
	}
}

