pipeline {
  agent {label 'kubepod'}
  
  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/htech7x/app-jenkins.git'
      }
    }
    
    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "pod.yaml", kubeconfigId: "mykubeconfig1")
        }
      }
    }
  }
}
