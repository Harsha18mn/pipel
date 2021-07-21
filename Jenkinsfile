pipeline {
	agent {label 'tag2'}  
	stages {
		stage('BUILD') {
      agent {label 'tag2'}
			steps {
				sh '''
					pwd
					sleep 5
					echo This is the fist stage: BUILD
				'''
			}	
		}
		
		stage('TEST') {
      agent {label 'tag1'}
			steps {
				sh '''
					pwd
					sleep 5
					echo This is the fist stage: TEST
				'''
			}	
		}
		
		stage('DEPLOY') {
      agent {label 'tag1'}
			steps {
				sh '''
					pwd
					sleep 5
					echo This is the fist stage: DEPLOY
				'''
			}	
		}
	}
}
