node {
	withEnv(["JEST_JUNIT_OUTPUT=output/coverage/junit/junit.xml"]) {
    sh 'npm test'
  }
  junit 'output/coverage/junit/junit.xml'
}