pipeline {
    agent any
    stages {

        stage('clonegit') {
            steps {
                git credentialsId: '3232a051-78eb-4b41-95ae-cbaad89ea2fa', url: 'https://github.com/fernandokarnagi/simple-java-maven-app.git'
            }
        }

        stage('clean') {
           steps {
                sh 'mvn clean'
            }
        }

        stage('package') {
           steps {
                sh 'mvn package'
            }
        }

        stage('install') {
             steps {
                sh 'mvn install'
             }
        }
    }
}