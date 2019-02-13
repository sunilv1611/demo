#!/bin/groovy
pipeline {
    node {
      stages {
        stage ('tests') {
          steps {
            sh 'npm test -- --ci --testResultsProcessor="jest-junit"'
            junit 'output/coverage/junit/junit.xml'
          }
        }
        stage('build') {
            steps {
                sh 'npm 6.4.1'
            }
        }
    }
  }
}