pipeline {
  agent any
  stages {
    stage('checkout project') {
      steps {
        checkout scm
      }
    }
    stage('test') {
      steps {
        sh 'mvn test'
      }
    }
    stage('package') {
      steps {
        sh '''mvn package
'''
      }
    }
    stage('deploy') {
      steps {
        sh '''make deploy-default
'''
      }
    }
  }
}