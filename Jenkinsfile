//pipeline {
//  agent any
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
    stage('send email') {
      steps {
        mail(subject: 'hello rich', body: 'hello rich', bcc: 'qiaorui.chen@meowlomo.com')
      }
    }
    stage('maven build') {
      steps {
//        sh 'mvn clean install'
      }
    }
  }
  environment {
    meow = 'rich'
  }
}
