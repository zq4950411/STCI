pipeline {
  agent any
  stages {
    stage('CheckOut') {
      steps {
        svn(url: 'svn://zhaiqiang@47.96.1.255/ppgame/app/STApp/iOS', changelog: true, poll: true)
      }
    }
    stage('Build') {
      steps {
        sh 'echo "Build"'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deploy"'
      }
    }
  }
}