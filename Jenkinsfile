pipeline {
	agent any

	stages{

		stage('Prepare'){
			steps{
				sh 'npm install  -g newman'
			}
		}
		stage('Test'){
			steps{
				sh 'newman run'
			}
		}
	}
	post{
		always{
			archiveArtifacts artifacts: '**/newman/*.html', allowEmptyArchive:true
		}
	}
}
