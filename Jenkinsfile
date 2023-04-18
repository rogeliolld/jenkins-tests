pipeline {
  agent any
  tools {
    nodejs 'node-18.14.2'
  }

  options {
    timeout(time: 2, unit: 'MINUTES')
  }

  stages {
    stage('Install dependencies') {
      steps {
        sh 'npm install'
      }
    }
    stage('Run tests') {
      steps {
        sh 'cd test && npm test'
      }
    }
  }
}
