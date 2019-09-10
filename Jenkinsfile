pipeline {
  agent any
  stages {
    stage('Gradle Build') {
      steps {
        sh '/var/lib/cloudbees-jenkins-distribution/workspace/SpringTestApp_master/gradlew build'
      }
    }
    stage('Push to PCF') {
      steps {
        pushToCloudFoundry(target: 'https://api.pcfsys.hms.hmsy.com', organization: 'DevOpsTesting', cloudSpace: 'App1', credentialsId: 'devopsuser1', selfSigned: 'Yes')
      }
    }
  }
}