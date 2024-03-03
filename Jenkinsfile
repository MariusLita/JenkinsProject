pipeline {
	agent any
	tools{
		maven "MAVEN3"
		jdk "openJDK11"
	}
	stages{
		stage('Fetch Code'){
			steps {
				git branch: 'master', url: 'https://github.com/MariusLita/JenkinsProject.git'
			}
		}
		stage('Build'){
			steps{
				sh 'mvn install -DskipTests'
			}
			
			post {
				success {
					echo 'Archiving artifacts now.'
					archiveArtifacts artifacts: '**/*.jar'
				}
			}
		}
		stage('UNIT TEST'){
			steps {
				sh 'mvn test'
			}
		}
	}
}