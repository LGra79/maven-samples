pipeline {
  agent any

  tools {
    maven 'DHT_MVN'
  }

  stages {
    stage('Build') {
      steps {
        script {
          def mvnHome = tool 'DHT_MVN'
          sh "${mvnHome}/bin/mvn clean test verify"
        }
      }
    }
  }
}