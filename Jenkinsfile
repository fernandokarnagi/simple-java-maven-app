pipeline {
    agent none
    stages {

        stage('clonegit') {
            agent {
                label 'mvn3'
            }
            steps {
                withCredentials([usernamePassword(credentialsId: 'mycompany-cred', passwordVariable: 'mypassword', usernameVariable: 'myuser')]) {
                    echo "My user is ${myuser} and pwd is ${mypassword}"
                }
                git credentialsId: '3232a051-78eb-4b41-95ae-cbaad89ea2fa', url: 'https://github.com/fernandokarnagi/simple-java-maven-app.git'
            }
        }

        stage('clean') {
            agent {
                label 'mvn3'
            }
           steps {
                sh 'mvn clean'
            }
        }

        stage('package') {
            agent {
                label 'mvn3'
            }
           steps {
                sh 'mvn package'
            }
        }

        stage('install') {
            agent {
                label 'mvn3'
            }
             steps {
                sh 'mvn install'
             }
        }
    }
}