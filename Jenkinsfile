#!/bin/groovy
pipeline {
    agent { docker { image 'node:6.3' } }
    
    stages {
        stage ('tests') {
          steps {
            sh 'npm test -- --ci --testResultsProcessor="jest"'
            junit 'output/coverage/junit/junit.xml'
          }
        }
    }
}