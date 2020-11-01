pipeline {
    agent any
    environment {
        PROJECT_ID = 'dev-hachiko-2020'
        CLUSTER_NAME = 'hachiko-cluster'
        LOCATION = 'us-central1-c	'
        CREDENTIALS_ID = 'dev-hachiko-2020'
    }
    stages {
        stage('Deploy to GKE') {
            steps{
                step([
                $class: 'KubernetesEngineBuilder',
                projectId: env.PROJECT_ID,
                clusterName: env.CLUSTER_NAME,
                location: env.LOCATION,
                manifestPattern: 'examples/5-1-kuard-pod.yaml',
                credentialsId: env.CREDENTIALS_ID,
                verifyDeployments: true])
            }
        }
    }
}
