#!/bin/groovy
pipeline {
    agent any
    
    stages {
        stage ('tests') {
          steps {
            sh 'jest --coverage --coverageDirectory=output/coverage/jest'
            junit 'output/coverage/junit/junit.xml'
          }
        } 
    }
}