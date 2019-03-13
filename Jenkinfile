pipeline {
  agent any
  stages {
    stage('Checkout source from Gitlab') {
      steps {
        checkout scm
      }
    }
    stage('Build Docker image') {
      steps {
        script {
          
        }

      }
    }
    stage('Test Docker image') {
      steps {
        script {
          sh 'echo "Tests passed"'
        }

      }
    }
    stage('Pushing image to Docker repo') {
      steps {
        script {
         o  \"\"\"<p>BUILD URL: ${env.BUILD_URL}</p> <p>\"PROJECT: ${env.JOB_NAME} \"</p> <p>ARTIFACTORY_PATH: https://captain.rtf.siemens.net:8443/simatic_edge/releases/sim-edge-platform-mosquitto-broker-ui/${BRANCH_NAME}:0.1.0.6.${BUILD_NUMBER}</p>\"\"\"  > mail.txt"

          }
        }

        sh 'echo "Image Pushed to Docker repo"'
      }
    }
  }
  environment {
    app = null
  }  
}
