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
	//agent any
	agent {docker {iamge 'maven:3.6.3'}}
	stages{
		stage('Build'){
			steps{
				sh "mvn --version"
				echo "build stage"
			}
		}
			stage('Test'){
				steps{
					echo "test"
				}
				
			}
			stage('release'){
				steps{
					echo "release"
				}
				
			}		
	} 
	post {
		always{
			echo 'hitting always'
		}
		success{
			echo 'success'
	
		}
		failure{
			echo 'build failed'
		}
	}

}
