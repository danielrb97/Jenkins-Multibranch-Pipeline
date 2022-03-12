pipeline {
	agent any
		stages {
			stage('first') {
				steps {
					script {
						env.TEST_VARIABLE='True'
					}
				}
			}
			stage('second') {
				when{
					env.TEST_VARIABLE 'True'
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
