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
            emailext(subject: 'test', body: 'succès', from: 'me', to: 'fa_bouali@esi.dz')
          }
        }
      }
    }
  }
}