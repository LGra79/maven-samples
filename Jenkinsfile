pipeline {
  agent any

  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }

  stages {
    stage('Build') {
      steps {
        sh """
          export PATH=${tool 'DHT_MVN'}/bin:\$PATH
          mvn clean test verify
        """
      }
    }
  }
}