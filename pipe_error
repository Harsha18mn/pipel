pipeline {
	agent {label 'mast'}  
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
     			//agent any
			parallel {
				stage('deploy1') {
					agent {label 'tag1'}
					steps {
						sh '''
						sleep 15
						echo This is the fist stage: DEPLOY1
						'''
					}
				}
				stage('deploy2') {
					agent {label 'tag2'}
					steps {
						sh '''
						sleep 15
						echo This is the fist stage: DEPLOY2
						'''
					}
				}
				stage('deploy3') {
					agent {label 'mast'}
					steps {
						sh '''
						sleep 15
						echo This is the fist stage: DEPLOY3
						'''
					}
				}
			}
		}
	}
}
