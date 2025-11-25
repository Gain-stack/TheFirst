pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/Gain-stack/TheFirst', branch: 'dev')
      }
    }

    stage('Shell') {
      parallel {
        stage('Shell') {
          steps {
            sh 'ls -la'
          }
        }

        stage('echo') {
          steps {
            sh 'echo \'hello world\''
          }
        }

      }
    }

  }
}