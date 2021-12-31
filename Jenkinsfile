pipeline {
  agent any
  stages {

    stage('clean') {
        steps {
            git credentialsId: '3232a051-78eb-4b41-95ae-cbaad89ea2fa', url: 'https://github.com/fernandokarnagi/simple-java-maven-app.git'
        }
    }

    stage('clean') {
      parallel {
        stage('clean') {
          steps {
            sh 'mvn clean'
          }
        }

        stage('cleaning') {
          steps {
            echo 'cleaning'
          }
        }

      }
    }

    stage('package') {
      parallel {
        stage('package') {
          steps {
            sh 'mvn package'
          }
        }

        stage('packaging') {
          steps {
            echo 'packaging'
          }
        }

      }
    }

    stage('install') {
      parallel {
        stage('install') {
          steps {
            sh 'mvn install'
          }
        }

        stage('Installing') {
          steps {
            echo 'Installing'
          }
        }

      }
    }

  }
}