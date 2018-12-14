pipeline {
  agent {
    docker {
      image 'python:2.7'
      args '-v ${PWD}:/docs'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'mkdocs build'
      }
    }
    stage('Test') {
      steps {
        sh 'ls -l site/'
      }
    }
    stage('Package') {
      steps {
        sh 'zip -r site.zip site/*'
      }
    }
    stage('Deliver') {
      steps {
        sh 'echo "Working on Delivry"'
      }
    }
  }
}