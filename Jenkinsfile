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
							  ls -al
						}
				}
				stage("Test"){
						steps{
								echo "========executing Test========"
							  ls -al
						}
				}
				stage("Staging"){
						steps{
								echo "========executing Staging Deploy========"
							  ls -al
						}
				}
				stage("Production"){
						steps{
								echo "========executing Production Deploy========"
							  ls -al
						}
				}
		}
}