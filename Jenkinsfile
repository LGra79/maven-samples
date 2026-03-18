pipeline {
  agent any

  stages {
    stage('Build') {
      steps {
        sh '/opt/homebrew/opt/maven/bin/mvn clean test verify'
      }
    }
  }
}