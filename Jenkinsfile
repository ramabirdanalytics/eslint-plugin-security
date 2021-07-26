pipeline {
  agent {
    docker {
      image 'bkimminich/juice-shop'
      args '3001:3000'
    }

  }
  stages {
    stage('Build') {
      steps {
        sh 'npm install --save-dev eslint-plugin-security'
      }
    }

    stage('Test') {
      steps {
        sh 'npm test'
      }
    }

  }
}