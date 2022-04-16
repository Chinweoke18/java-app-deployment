pipeline {
	agent any
    stages {
        stage('Build on k8 ') {
            steps {           
                        sh 'pwd'
                        sh 'aws sts get-caller-identity'
                        sh 'export AWS_PROFILE="clusteradmin"'
                        sh 'aws sts get-caller-identity'
                        sh 'cp -R helm/* .'
		        sh 'ls -ltr'
                        sh 'pwd'
                        sh 'helm install java-app petclinic --set image.repository=chinweoke/java-app --set image.tag=13'
              			
            }           
        }
    }
}