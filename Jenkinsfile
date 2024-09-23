pipeline {
    agent any
    tools {
        jdk 'jdk17'
        nodejs 'node16'
    }
    environment {
        SCANNER_HOME = tool 'sonar-scanner'
    }
    stages {
        stage('Clean Workspace') {
            steps {
                cleanWs()
            }
        }
        stage('Checkout from Git') {
            steps {
               git url: 'https://github.com/rukmini-jadhav/a-reddit-clone.git', branch: 'main'

            }
        }
        stage('Sonarqube analysis') {
            steps {
                withSonarQubeEnv('SonarQube-Server') {
                    sh '''$SCANNER_HOME/bin/sonar-scanner \
                -Dsonar.projectName=Reddit-CloneCI \
                -Dsonar.projectKey=Reddit-Clone-CI'''
                }

            }
        }
    }

}
