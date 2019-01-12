pipeline {
  agent any
  options {
        timeout(time: 10, unit: 'MINUTES') // 10 minutes de timeout
        quietPeriod(30) // temps d'attente avant l'exécution
        retry(3) // ré-essayer 3 fois en cas d'échec
        }
  
  stages {
    stage('sending mail') {
      steps {
        timeout(time: 200, unit: 'SECONDS') {
          emailext(subject: 'test2', body: 'yeeeessss', to: 'fa_bouali@esi.dz', from: 'fa_bouali@esi.dz') 
        }
      }
    }
  }
}
