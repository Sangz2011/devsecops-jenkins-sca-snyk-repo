pipeline {
  agent any
  tools { 
        maven 'Maven_3_9_6'  
    }
   stages{
    stage('RunSCAAnalysisUsingSnyk') {
            steps {		
				withCredentials([string(credentialsId: 'SNYK_TOKEN', variable: 'SNYK_TOKEN')]) {
					sh 'mvn snyk:test -fn'
				}
			}
	
    }		
  }
}
