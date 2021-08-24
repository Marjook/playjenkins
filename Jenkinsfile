pipeline {

  agent { label 'kubepod' }

  stages {

    stage('Checkout Source') {
      steps {
        git url:'https://github.com/marjook/playjenkins.git'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "valaxydeploy.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
