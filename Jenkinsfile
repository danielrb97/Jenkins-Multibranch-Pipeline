pipeline {
	agent any
		stages {
			stage('first') {
				steps {
					script {
						env.VARIABLE="True"
					}
				}
			}
			stage('second') {
				when{
					${VARIABLE}="True"
				}
				steps {
					script {
						echo ${VARIABLE}
					}
				}
			} 

			stage('third') {
				steps {
					sh 'echo "Step Three"'
				}
			}
		}
}
