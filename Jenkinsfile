pipeline {
	agent any
		stages {
			stage('first') {
				steps {
					script {
						env.IS_BOOLEAN=True
					}
				}
			}
			stage('second') {
				when{
					env.IS_BOOLEAN = True
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
