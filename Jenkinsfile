pipeline {
    agent any
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
    }
}
