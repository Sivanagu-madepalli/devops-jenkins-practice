node {
	agent any
	//agent{docker(image 'maven:3.6.3')}
	//agent{docker(image 'node:13.8')}
	stages{
		stage('Build'){
			steps{
				//sh 'maven --version'
				//sh 'node --version'
				echo "Build"
			}
		}
		stage('Test'){
			steps{
				echo "Test"
			}
		}
		stage('Integration Test'){
			steps{
				echo "Integration Test"
			}
		}
	}

	post{
		always{
			echo "Running always"
		}
		success{
			echo "running when successful"
		}
		failure{
			echo "running when fail"
		}
	}
}
