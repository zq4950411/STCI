pipeline {
  agent any
  stages {
    stage('CheckOut') {
        environment {
            username:password = crea('c65fcf11-b58c-46a3-b7bd-1464feefe5f7')
        }
        steps {
            sh 'printenv'
            sh 'svn://47.96.1.255/ppgame/app/STApp/iOS/ShuTiao/trunk --username zhaiqiang --password nacaizq'
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