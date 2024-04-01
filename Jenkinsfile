pipeline {
    agent any
    
    environment {
        KUBECONFIG_CREDENTIAL_ID = 'demo-kubeconfig'
        GITHUB_CREDENTIAL_ID = 'github-id'
        GITHUB_ACCOUNT = 'mansha-arora'
    }

    stages {
        stage('Deploy Manifests') {
            steps {
            // input(id: 'deploy-to-production', message: 'deploy to production?')
            // container ('maven') {
            //     withCredentials([
            //         kubeconfigFile(
            //         credentialsId: env.KUBECONFIG_CREDENTIAL_ID,
            //         variable: 'KUBECONFIG')
            //         ]) {
                    sh 'envsubst < inner-data/kubesphere/pipelines/apisix-routes.yaml | kubectl apply -f -'
                }
            }
            }
        }