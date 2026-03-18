pipeline {
  agent any

  tools {
    maven 'DHT_MAVEN'
  }

  stages {
    stage('Build') {
      steps {
        script {
          def mvnHome = tool 'DHT_MAVEN'
          sh "${mvnHome}/bin/mvn clean test verify"
        }
      }
    }
  }
}