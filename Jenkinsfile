pipeline {

  environment {
    registry = "dockernaveensddp/my-app"
    dockerImage = ""
  }

  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/justmeandopensource/playjenkins.git'
      }
    }

    stage('Build image') {
      steps{
        script {
          dockerImage = docker.build registry + ":$BUILD_NUMBER"
        }
      }
    }

<<<<<<< HEAD
=======
    
>>>>>>> 4a712ee758bcf5323353394e00b18e14fd8d2089

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "deploy/*", kubeconfigId: "e2d7f6bc-22fc-4ce3-94db-9fe04d4c69b4")
        }
      }
    }

  }

}
