pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git(url: 'https://github.com/Gain-stack/TheFirst', branch: 'master')
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

    stage('Build') {
      steps {
        sh 'docker build .'
      }
    }

  }
}