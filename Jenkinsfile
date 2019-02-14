#!/bin/groovy
pipeline {
    any
    
    stages {
        stage ('tests') {
          steps {
            sh 'npm test -- --ci'
            junit 'output/coverage/junit/junit.xml'
          }
        }
    }
}