pipeline {
    agent any
    stages{
        stage('clean workspace') {
            steps {
                cleanWs ()
            }
        }
        stage('checkout from git') {
            steps {
                git branch: 'main', git url: 'https://github.com/rukmini-jadhav/a-reddit-clone.git'
            }
        }
    }
}
