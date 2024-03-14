pipeline {
    agent any
    stages {
        stage ('compile-package') {
            steps {
                //get maven home path
                def mvnHome = tool name: 'maven-3', type: 'maven'
                sh "${mvnHome}/bin/mvn package"                
            }  
        }
        stage ('StaticCodeAnalysis') {
            steps {
                def mvnHome = tool name: 'maven', type: 'maven'
	              withSonarQubeEnv('Sonarqube') {
	                  sh "${mvnHome}/bin/mvn sonar:sonar"
                }  
            }  
        }      
    }  
}
  
