
pipeline {
    agent { docker { image 'node:6.3' } }
    
    stages {
      stage ('tests') {
            withEnv(["JEST_JUNIT_OUTPUT=output/coverage/junit/junit.xml"]) {
            sh 'npm test -- --ci --testResultsProcessor="jest-junit"'
            }
            junit 'output/coverage/junit/junit.xml'
        }
    }
}