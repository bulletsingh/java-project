pipeline{
   agent any
   stages{
	
	stage('Unit Tests'){
	steps{
		sh 'ant -f test.xml -v'
		junit 'reports/result.xml'
	}
	}
	stage('build'){

	steps{
	sh 'ant -f build.xml'
			}
		}
	}
   post {
	always {
	archiveArtifacts artifacts: 'dist/*.jar', fingerprint: true
	
	}
}
}
