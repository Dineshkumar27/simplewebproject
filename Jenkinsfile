pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
               git 'https://github.com/Dineshkumar27/simplewebproject.git'
            }
        }
        stage('Maven build') {
            steps {
               sh "${MAVEN_HOME}/bin/mvn clean install"
            }
        }
    }
}
