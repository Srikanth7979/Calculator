pipeline {
    agent any
    tools {
        maven 'Maven3'        //name give in managejenkins > tools > maven (section) > name: Maven3
    }    
    stages {
        stage ('compile-package') {
            steps {
                script {
                    //get maven home path
                    
                    //sh "mvn clean compile"
                    sh "mvn clean package"
                    //sh "mvn clean install"
                }
            }
        }
        stage ('StaticCodeAnalysis') {
            steps {
                script {
                    //def mvnHome = tool name: 'maven', type: 'maven'
                    //withSonarQubeEnv('Sonarqube') {
                        //sh "mvn sonar:sonar"}
                    echo "static analaysis stage"
                    
                }
            }
        }
    }
}

  
