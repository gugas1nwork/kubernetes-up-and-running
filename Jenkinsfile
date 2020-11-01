pipeline {

  agent any

  stages {
    
    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "examples/5-1-kuard-pod.yaml", kubeconfigId: "hachiko-cluster")
        }
      }
    }

  }

}
