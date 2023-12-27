pipeline{
		agent any
		// agent { docker { image 'maven:3.6.3' } }

		// environment {
		// 	dockerHome = tool 'docker'
		// 	mavenHome = tool 'mvn'
		// 	PATH = ""
		// }
		stages{
				stage("A"){
						steps{
								echo "========executing A========"
								echo "ls -al"
						}
						// post{
						// 		always{
						// 				echo "========always========"
						// 		}
						// 		success{
						// 				echo "========A executed successfully========"
						// 		}
						// 		failure{
						// 				echo "========A execution failed========"
						// 		}
						// }
				}
		}
		// post{
		// 		always{
		// 				echo "========always========"
		// 		}
		// 		success{
		// 				echo "========pipeline executed successfully ========"
		// 		}
		// 		failure{
		// 				echo "========pipeline execution failed========"
		// 		}
		// }
}