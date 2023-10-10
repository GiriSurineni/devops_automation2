pipeline {
    agent any
    tools {
        maven 'maven'
    }
    stages {
        stage ('build docker hello world img'){
            steps{
                script{
                    sh 'docker build -t sgiriprasad/hello-world.'
                }
            }
        }
        stage ('push image to hub'){
            steps{
                script{
                    withCredentials([string(credentialsId: 'dockerhubcred', variable: 'dockerpwd')]) {
                    sh 'docker login -u sgiriprasad -p ${dockerhubcred}'
}
                    sh 'docker push sgiriprasad/devops-automation2'
                }
            }
        }
    }
}