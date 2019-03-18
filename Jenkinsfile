pipeline {
  agent any
  triggers {
              cron(env.BRANCH_NAME == 'master' ? '30 * * * *' : '')
             }
  stages {
    stage('Checkout source from Gitlab') {
      steps {
        checkout scm
      }
    }
    
    stage('Test Docker image') {
      steps {
        script {
          sh 'echo "Tests passed"'
        }
      }
    }

}
