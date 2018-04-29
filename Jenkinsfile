pipeline {
  agent any
  stages {
    stage('Testing') {
      failFast true
      parallel {
        stage('Java 7') {
          agent {
            label 'jdk7'
          }
          steps {
            sh 'java -version'
            sleep(time: 10, unit: 'SECONDS')
          }
        }
        stage('Java 8') {
          agent {
            label 'jdk8'
          }
          steps {
            sh 'java -version'
            sleep(time: 20, unit: 'SECONDS')
          }
        }
      }
    }
  }
}