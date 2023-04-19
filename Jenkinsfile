pipeline {
  agent any
  stages {
    stage('Checkout code') {
      steps {
        git(url: 'https://github.com/Mahendra1452/git-tutorial/', branch: 'master')
      }
    }

    stage('log') {
      parallel {
        stage('log') {
          steps {
            sh 'ls -la'
          }
        }

        stage('Front-end unit tests') {
          steps {
            sh 'npm i && npm install express -g'
          }
        }

      }
    }

  }
}