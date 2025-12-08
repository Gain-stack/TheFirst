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
        sh 'docker build . -t duszap/jenkins:1'
      }
    }

    stage('Login') {
      environment {
        DOCKER_USERNAME = ''
        DOCKER_PASSWORD = ''
      }
      steps {
        sh 'docker login -u $DOCKER_USERNAME -p $DOCKER_PASSWORD'
      }
    }

    stage('Push') {
      steps {
        sh 'docker push duszap/jenkins:1'
      }
    }

  }
}
