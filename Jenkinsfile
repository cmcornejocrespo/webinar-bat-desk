node {
    def branchName = env.BRANCH_NAME	
   		
	stage('build-and-test') {
		steps {
			withMaven() {
				sh 'mvn clean install -Pall-test'
			}
		}
	}
	
	if(branchName != 'master') {
	
		stage('deploy-integration-environment') {
		
		
		}
		
		stage('integration-test') {
			
			withMaven() {
				//sh 'mvn clean install -Pintegration-tests'
			}
			
		}			
		
		stage('release-to-master) {
		
		}
	}else {	
		stage('deploy-nexus) {
			
		}
		
		stage('deploy-production) {
		
		}
	}    	
}