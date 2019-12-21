pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build Started'
        sh 'mvn -Dmaven.test.failure.ignore clean package'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing Phase'
        junit '\'**/target/surefire-reports/TEST-*.xml\''
      }
    }

  }
}