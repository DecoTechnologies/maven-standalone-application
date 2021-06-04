// Powered by Infostretch 

timestamps {

node () {

	stage ('Paypal-Java-App - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'git-credentials', url: 'https://github.com/DecoTechnologies/maven-standalone-application']]]) 
	}
	stage ('Paypal-Java-App - Build') {
 			// Maven build step
	withMaven(maven: 'maven') { 
 			if(isUnix()) {
 				sh "mvn clean package " 
			} else { 
 				bat "mvn clean package " 
			} 
 		} 
	}
}
}