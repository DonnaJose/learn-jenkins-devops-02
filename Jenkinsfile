//Declarative pipeline
pipeline{
	
	agent any
	// agent{
	// 	docker{
	// 		image 'maven:3.9.9'
	// 	}
	// }
	environment{
		myDockerHome= tool 'myDocker'
		myMavenHome= tool 'myMaven'
		PATH="$myDockerHome/bin:$myMavenHome/bin:$PATH"
	}
	stages{
		stage('Build-03'){
			steps{
				//sh 'mvn clean install'
				sh 'docker  version'
				sh 'mvn --version'
				sh 'Build tage= $env.BUILD_TAG'
				echo "Build 03"
			}
		}
		stage('Compile'){
			steps{
				sh 'mvn clean compile'
			}
		}
		// stage('Test'){
		// 	steps{
		// 		sh 'mvn test'
		// 	}
		// }
		// stage ('Integration Test'){
		// 	steps{
		// 		sh 'mvn failsafe:integration-test failsafe:verify'
		// 	}
		// }
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

