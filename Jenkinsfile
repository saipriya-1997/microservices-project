pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                sh 'docker build -t saipriya129/productcatalogservice:v1 .'
            }
        }
        stage("push") {
            steps {
                script {
                    withDockerRegistry(credentialsId: 'docker-cred') {
                      sh 'docker push saipriya129/productcatalogservice:v1'
                    }
                }
            }
        }
    }
}
