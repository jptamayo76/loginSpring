pipeline {
    agent any
    tools {
       maven 'maven-3.9.2' 
    }
    stages {
        stage('Git') {
            steps {
                echo 'GIT stage'
                git branch: 'main', credentialsId: 'SSH-KEY-admin-DESKTOP', url: 'https://github.com/jptamayo76/loginSpring.git'		
            }
        }
        stage('Maven') {
            steps {
                echo 'Maven stage'

                // Run Maven on a Unix agent.
                //sh "mvn -Dmaven.test.failure.ignore=true clean package"

                // To run Maven on a Windows agent, use
                bat "mvn -Dmaven.test.failure.ignore=true clean package"

            }
        }        
    }
}