pipeline{
			agent any
			environment{
				MODULE = 'vpc'
				ACTION = 'apply'
				}

		stages{	
				stage('Validate')
				{
					steps{
					sh 'chmod +x ./scripts/validate.sh'
					sh './scripts/validate.sh'
					}
				}
				stage('Init')
				{
					steps{
					sh 'chmod +x ./scripts/init.sh'
					sh './scripts/init.sh'
					}
				}
				stage('Plan & Apply')
				{
					steps{
					sh 'chmod +x ./scripts/apply.sh'
					sh './scripts/apply.sh'
					}
				}
				stage('Post apply')
				{
					steps{
					sh 'chmod +x ./scripts/postapply.sh'
					sh './scripts/postapply.sh'
					}
				}
				stage('Pre Destroy')
				{
					steps{
					sh 'chmod +x ./scripts/predestroy.sh'
					sh './scripts/predestroy.sh'
					}
				}
				stage('Destroy')
				{
					steps{
					sh 'chmod +x ./scripts/destroy.sh'
					sh './scripts/destroy.sh'
					}
				}																				
			}
		}