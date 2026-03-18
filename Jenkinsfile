pipeline {
  agent any

  tools {
    maven 'DHT_MAVEN'
    jdk 'DHT_SENSE'
  }

  stages {
    stage('Build') {
      steps {
        sh 'mvn clean test verify -Dmaven.compiler.release=11'
      }
    }
  }
}