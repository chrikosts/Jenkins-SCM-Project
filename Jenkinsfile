// This should be a comment
pipeline {
  agent any
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '7', numToKeepStr: '14')
    disableConcurrentBuilds()
  }
  stages {
    stage('Hello') {
      steps {
        sh 'echo Hello World'
        echo "Build number is ${currentBuild.number}"
      }
    }
  }
}
