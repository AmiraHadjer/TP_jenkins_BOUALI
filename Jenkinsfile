pipeline {
  agent any
  stages {
    stage('sending mail') {
      steps {
        mail(subject: 'test', body: 'succès', from: 'fa_bouali@esi.dz', to: 'fa_bouali@esi.dz')
      }
    }
  }
}