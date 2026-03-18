// pipeline {
//   agent any

//   tools {
//     maven 'DHT_MAVEN'
//     jdk 'DHT_SENSE'
//   }

//   stages {
//     stage('Build') {
//       steps {
//         sh 'mvn clean test verify -Dmaven.compiler.release=11'
//       }
//     }
//   }
// }
pipeline {
  agent any

  tools {
    maven 'DHT_MAVEN'
    jdk 'DHT_SENSE'
  }

  stages {
    stage('Bisect') {
      steps {
        sh '''
          git bisect start 198644632661c67b6c32f59e9047c11a70685e15 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5
          git bisect run mvn clean test
        '''
      }
    }
  }
}