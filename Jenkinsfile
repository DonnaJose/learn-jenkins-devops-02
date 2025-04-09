//Declarative pipeline
pipeline{
	
	//agent any
	agent{
		docker{
			image 'node:13.8'
		}
	}
	stages{
		stage('Build-03'){
			steps{
				sh 'docker  version'
				sh 'node --version'
				echo "Build 03"
			}
		}
		stage('Test-03'){
			steps{
				echo "Test 03"
			}
		}
		stage('Int-Test-03'){
			steps{
				echo "Int-test 03"
			}
		}
	}
	post{
		always{
			echo "Run always 03"
		}
		success{
			echo "succesfully built"
		}
		failure{
			echo "failed"
		}
		changed{
			echo "changed"
		}
	}
}
// Scripted pieline where stages are optional
// node {
	
// 		echo "Build 01"
// 		echo "Test-01"
// 		echo "Int-Test-01"
// 	}
	

// node {
// 	stage('Build') {
// 		echo "Build 01"
// 	}
// 	stage('Test') {
// 		echo "Test-01"
// 	}
// 	stage('Integeration Test') {
// 		echo "Int-Test-01"
// 	}
// }

