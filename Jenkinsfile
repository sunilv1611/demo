#!/bin/groovy
pipeline {
    agent {label 'node'}
    
    stages {
        stage ('tests') {
          steps {
            sh 'npm test -- --ci --testResultsProcessor="jest-junit"'
            junit 'output/coverage/junit/junit.xml'
          }
        }
    }
}