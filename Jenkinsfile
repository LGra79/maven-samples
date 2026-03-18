pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh """
          export PATH=/opt/homebrew/opt/maven/bin:\$PATH
          mvn clean test verify
        """
      }
    }
  }
}