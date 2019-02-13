#!/bin/groovy
pipeline {
    agent { docker { image 'node:10.14.1' } }
    
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