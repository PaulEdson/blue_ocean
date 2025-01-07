pipeline {
  agent {
    node {
      label 'docker'
    }

  }
  stages {
    stage('git') {
      steps {
        git(url: 'https://github.com/PaulEdson/blue_ocean', branch: 'main')
      }
    }

    stage('build') {
      steps {
        sh 'docker build -t pauljedson/blue .'
      }
    }

  }
}