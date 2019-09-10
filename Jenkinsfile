pipeline {
  agent any
  stages {
    stage('Gradle Build') {
      steps {
        sh '/var/lib/cloudbees-jenkins-distribution/workspace/SpringTestApp_master/gradlew build'
      }
    }
  }
}