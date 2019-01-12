pipeline {
  agent any
  stages {
    stage('sending mail') {
      steps {
        timeout(time: 200, unit: 'SECONDS') {
          emailext(subject: 'test2', body: 'yeeeessss')
        }

      }
    }
    stage('hello') {
      steps {
        echo 'hello'
      }
    }
  }
  options {
    timeout(time: 10, unit: 'MINUTES')
    quietPeriod(30)
    retry(3)
  }
}