pipeline {
  agent any

  tools {
        maven 'mymaven' // Must match the name configured in Jenkins Tools
    }
  
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/AkashMalik002/sample-maven-project.git'
      }
    }
    stage('Build') {
      steps {
        sh 'mvn clean compile'
      }
    }
    stage('Test') {
      steps {
        sh 'mvn test'
      }
    }
    stage('Package') {
      steps {
        sh 'mvn package'
      }
    }
  }
}
