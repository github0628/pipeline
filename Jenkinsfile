pipeline {
  agent any
  stages {
    stage('checkout') {
      agent {
        node {
          label 'build'
        }

      }
      steps {
        svn(url: 'svn://cqr@localhost:8082', changelog: true, poll: true)
      }
    }
  }
}