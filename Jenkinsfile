stage ('tests') {
  withEnv(["JEST_JUNIT_OUTPUT=./jest-test-results.xml"]) {
    sh 'npm test -- --ci --testResultsProcessor="jest-junit"'
  }
  junit 'jest-test-results.xml'
}