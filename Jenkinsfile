pipeline {
  agent any
  stages {
    stage('Build') {
      post {
        always {
          echo 'Build stage complete'

        }

        failure {
          echo 'Build failed'

        }

        success {
          echo 'Build succeeded'

        }

      }
      steps {
        bat 'C:\\gradle-4.10.2-all\\gradle-4.10.2\\bin\\gradle'
      }
    }
    stage('sending mail') {
      parallel {
        stage('sending mail') {
          steps {
            timeout(time: 200, unit: 'SECONDS') {
              emailext(subject: 'test2', body: 'yeeeessss', replyTo: 'fa_bouali@esi.dz', to: 'amihadjer@gmail.com')
            }

          }
        }
        stage('sonarQ') {
          steps {
            withSonarQubeEnv 'TP8'
          }
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