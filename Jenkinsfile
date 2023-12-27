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
							  sh "ls -al"
								sh "cd src"
								sh "ls -al"
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