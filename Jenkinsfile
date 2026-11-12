pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/mustafaumar/curriculum-app/', branch: 'master')
      }
    }

    stage('error') {
      parallel {
        stage('error') {
          steps {
            sh '''ls -la
'''
          }
        }

        stage('Front-end Unit Tests') {
          steps {
            sh 'cd curriculum-front && npm -i && npm run test:unit'
          }
        }

      }
    }

  }
}