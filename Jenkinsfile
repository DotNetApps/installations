pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        echo 'checkout the code'
      }
    }
    stage('compile') {
      steps {
        echo 'compile the original source code'
      }
    }
    stage('compile test code') {
      steps {
        echo 'compile the test code'
      }
    }
    stage('junit test cases') {
      steps {
        echo 'run the junit test cases'
      }
    }
    stage('buil') {
      steps {
        echo 'build the package'
      }
    }
    stage('sonar') {
      steps {
        echo 'code quality check,code analysis'
      }
    }
    stage('Deploy to nexus') {
      parallel {
        stage('Deploy to nexus') {
          steps {
            echo 'deploying the nexus'
          }
        }
        stage('Deploy dev server') {
          steps {
            echo 'deploy the target server'
          }
        }
      }
    }
    stage('selenium test') {
      steps {
        echo 'automation test'
      }
    }
  }
}