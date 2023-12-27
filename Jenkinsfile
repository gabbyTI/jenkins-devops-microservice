pipeline{
		agent any
		// agent { docker { image 'maven:3.6.3' } }

		// environment {
		// 	dockerHome = tool 'docker'
		// 	mavenHome = tool 'mvn'
		// 	PATH = ""
		// }
		stages{
				stage("Build"){
						steps{
								echo "========executing Build========"
								echo "BUILD_NUMBER - $env.BUILD_NUMBER"
								echo "BUILD_ID - $env.BUILD_ID"
								echo "BUILD_DISPLAY_NAME - $env.BUILD_DISPLAY_NAME"
								echo "JOB_NAME - $env.JOB_NAME"
								echo "JOB_BASE_NAME - $env.JOB_BASE_NAME"
								echo "BUILD_TAG - $env.BUILD_TAG"
								echo "NODE_NAME - $env.NODE_NAME"
						}
				}
				stage("Test"){
						steps{
								echo "========executing Test========"
						}
				}
				stage("Staging"){
						steps{
								echo "========executing Staging Deploy========"
						}
				}
				stage("Production"){
						steps{
								echo "========executing Production Deploy========"
						}
				}
		}
}