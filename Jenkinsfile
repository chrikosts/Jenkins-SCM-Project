// This should be a comment...
pipeline {
  agent any
  triggers {
    cron '''TZ=Europe/Athens
  H */1 * * *'''
  }
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '7', numToKeepStr: '14')
    disableConcurrentBuilds()
  }
  stages {
    stage('Hello') {
      steps {
        bat 'echo Hello World'
        echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
        echo "Build number is ${currentBuild.number}"
      }
    }
  }
}
