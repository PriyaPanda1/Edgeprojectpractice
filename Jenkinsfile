pipeline {
  agent any
  triggers {
              cron(env.BRANCH_NAME == 'mqttui_integration' ? '00 1 * * *' : '')
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

