pipeline {
  agent any
  stages {
    stage('CheckOut') {
      steps {
        sh 'svn co svn://47.96.1.255/ppgame/app/STApp/iOS --username zhaiqiang --password nacaizq'
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