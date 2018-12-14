pipeline {
  agent {
    docker {
      image 'squidfunk/mkdocs-material'
      args '-v $WORKSPACE:/docs'
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