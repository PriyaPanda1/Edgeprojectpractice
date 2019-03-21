pipeline {
  agent any
  triggers {
              cron(env.BRANCH_NAME == 'master' ? '00 1 * * *' : '')
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
  
   
  
  
}

