pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'mvn clean install -Dmaven.compiler.source=21 -Dmaven.compiler.target=21'
      }
    }
    stage('Docker Build') {
      steps {
        sh 'docker build -t myapp:latest .'
      }
    }
  }
}
