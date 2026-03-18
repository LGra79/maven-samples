pipeline {
  agent any
  tools { 
      maven 'DHT_MVN' 
      jdk 'DHT_SENSE' 
  }
  stages {
    stage('Build') {
      steps {
        withEnv(["PATH+MAVEN=${tool 'DHT_MVN'}/bin"]) {
          sh 'mvn clean test verify'
        }
      }
    }
  }
}