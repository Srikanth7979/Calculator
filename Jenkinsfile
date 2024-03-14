pipeline {
    agent any
    stages {
        stage ('compile-package') {
            steps {
                script {
                    //get maven home path
                    
                    sh "mvn package"
                }
            }
        }
        stage ('StaticCodeAnalysis') {
            steps {
                script {
                    def mvnHome = tool name: 'maven', type: 'maven'
                    withSonarQubeEnv('Sonarqube') {
                        sh "mvn sonar:sonar"
                    }
                }
            }
        }
    }
}

  
