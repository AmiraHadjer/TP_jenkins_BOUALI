pipeline {
  agent any
  stages {
    stage('sending mail') {
      steps {
        timeout(time: 200, unit: 'SECONDS') {
          emailext(subject: 'test2', body: 'yeeeessss', replyTo: 'fa_bouali@esi.dz', to: 'amihadjer@gmail.com')
        }

      }
    }
    stage('hello') {
      steps {
        echo 'hello2'
      }
    }
  }
  options {
    timeout(time: 10, unit: 'MINUTES')
    quietPeriod(30)
    retry(3)
  }
}