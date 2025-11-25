pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/Gain-stack/TheFirst', branch: 'dev')
      }
    }

    stage('Shell') {
      steps {
        sh 'ls -la'
      }
    }

  }
}