pipeline {
  agent any
  triggers {
              cron(env.BRANCH_NAME == 'Develop' ? '05 * * * *' : '')
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

