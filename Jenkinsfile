pipeline {
  agent any
  stages {
    stage('error') {
      parallel {
        stage('error') {
          steps {
            echo 'hi'
          }
        }
        stage('') {
          steps {
            emailext(subject: 'test', body: 'succ�s', from: 'me', to: 'fa_bouali@esi.dz')
          }
        }
      }
    }
  }
}