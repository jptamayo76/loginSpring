pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                git branch: 'main', credentialsId: 'SSH-KEY-admin-DESKTOP', url: 'https://github.com/jptamayo76/loginSpring.git'		
            }
        }
        stage('Maven') {
            steps {
                echo 'Maven stage'
                mvn clean package
            }
        }        
    }
}