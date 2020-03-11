// node {
// 	stage('Build') {
// 		echo "Build"
// 	}
// 	stage('Test') {
// 		echo "Test"
// 	}
// 	stage('IntegrationTest') {
// 		echo "IntegrationTest"
// 	}
// }
//Declarative

pipeline {
	agent any
	//agent {docker {image 'maven:3.6.3'}}
	environment {
		dockerHome = tool 'myDocker'
		mavenHome = tool 'myMaven'
		PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
	}
	stages{
		stage('Build'){
			steps{
				sh 'mvn --version'
				sh 'docker version'
				echo "build stage"
			}
		}
	}
}
	// 		stage('Test'){
	// 			steps{
	// 				echo "test"
	// 			}
				
	// 		}
	// 		stage('release'){
	// 			steps{
	// 				echo "release"
	// 			}
				
	// 		}		
	// } 
	// post {
	// 	always{
	// 		echo 'hitting always'
	// 	}
	// 	success{
	// 		echo 'success'
	
	// 	}
	// 	failure{
	// 		echo 'build failed'
	// 	}
	// }


