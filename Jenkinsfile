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
	stages{
		stage('Build'){
			steps{
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
		
	}post{
		always{
			echo "hitting always"
		}
		success{
			echo "success"
	
		}
		failure{
			echo "build failed"
		}
	}

}
