#!/bin/groovy
pipeline {
    agent none
    
    stages {
        stage ('tests') {
          steps {
            sh 'npm test -- --ci --testResultsProcessor="jest-junit"'
            junit 'output/coverage/junit/junit.xml'
          }
        }
    }
}