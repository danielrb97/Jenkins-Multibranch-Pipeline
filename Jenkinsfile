pipeline {
	agent any
		stages {
			stage('first') {
				steps {
					script {
						env.BRANCH_NAME='True'
					}
				}
			}
			stage('second') {
				when{
					BRANCH_NAME 'True'
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
