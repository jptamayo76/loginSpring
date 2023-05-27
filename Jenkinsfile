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
                sh 'mvn clean package'
            }
        }        
    }
}