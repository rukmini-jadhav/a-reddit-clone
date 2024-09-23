pipeline {
    agent any
      stages {
        stage('clean workspace') {
            steps {
                cleanWs()
            }
        }
        stage('Checkout from Git') {
            steps {
                git branch: 'main', url: 'https://github.com/rukmini-jadhav/a-reddit-clone.git'
            }
        }
      }
}
