pipeline{
		agent any
		// agent { docker { image 'maven:3.6.3' } }

		environment {
			dockerHome = tool 'myDocker'
			mavenHome = tool 'myMaven'
			PATH = "$dockerHome/bin:$mavenHome/bin:$PATH"
		}
		stages{
				stage("checkout"){
						steps{
								echo "========executing checkout========"
								sh "docker version"
								sh "mvn --version"
								echo "BUILD_NUMBER - $env.BUILD_NUMBER"
								echo "BUILD_ID - $env.BUILD_ID"
								echo "BUILD_DISPLAY_NAME - $env.BUILD_DISPLAY_NAME"
								echo "JOB_NAME - $env.JOB_NAME"
								echo "JOB_BASE_NAME - $env.JOB_BASE_NAME"
								echo "BUILD_TAG - $env.BUILD_TAG"
								echo "NODE_NAME - $env.NODE_NAME"
						}
				}
				stage("Compile"){
						steps{
								sh "mvn clean compile"
						}
				}
				// stage("Test"){
				// 		steps{
				// 				sh "mvn test"
				// 		}
				// }
				// stage("Integration Test"){
				// 		steps{
				// 				sh "mvn failsafe:integration-test failsafe:verify"
				// 		}
				// }
				stage("Package"){
						steps{
								sh mvn package -DskipTests
						}
			
				}

				stage("Build Docker image"){
						steps{
								script {
									dockerImage = docker.build("gabelearn.azurecr.io/currency-exchange-devops:${env.BUILD_TAG}")
								}
						}
			
				}

				stage("Push Docker image"){
						steps{
								script {
									docker.withRegistry("gabelearn.azurecr.io", "azure_acr"){
										dockerImage.push();
										dockerImage.push("latest");
									}
								}
						}
			
				}
		}
}