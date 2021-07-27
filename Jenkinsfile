pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
               echo 'Git Checkout is Success'
            }
        }
        stage('Maven build') {
            steps {
               sh "${MAVEN_HOME}/bin/mvn clean install"
            }
        }
        stage('Archiving Artifacts'){
            steps{
                archiveArtifacts artifacts: 'target/*.war'
            }
        }
    }
}
