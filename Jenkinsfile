pipeline {
  agent any
  options { skipDefaultCheckout() }
  triggers { githubPush() }
  stages {
    stage('Checkout') {
      steps {
        dir('app') {
          checkout scm
        }
      }
    }
    stage('Build') {
      steps {
        dir('app') {
          sh 'echo "Files in app/:" && ls -l'
        }
      }
    }
  }
}
