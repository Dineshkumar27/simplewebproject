pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "MAVEN"
    }

    stages {
        stage('GET PROJECT FROM GIT') {
            steps {
               git 'https://github.com/Dineshkumar27/simplewebproject.git'
            }
        }
        stage('PACKAGING MAVEN PROJECT') {
            steps {
               bat "mvn clean package"
            }
        }
        stage('Deploye to tomcat') {
            steps {
               deploy adapters: [tomcat8(credentialsId: 'tomcat-login', path: '', url: 'http://localhost:8080/')], contextPath: 'simplewebproject', war: '**/*.war'
            }
        }
    }
}
