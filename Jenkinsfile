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

        stage('error') {
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

        stage('error') {
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

        stage('error') {
          steps {
            echo 'Installing'
          }
        }

      }
    }

  }
}