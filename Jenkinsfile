pipeline {
  agent any
  stages {
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