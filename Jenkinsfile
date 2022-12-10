pipeline {
    agent any
    stages {
        stage('docker build') {
            steps {
               script {
                sh "docker build -f Jenkins/Dockerfile -t adrianyaniri/disenio-industrial:latest-${BUILD_NUMBER} ."
               }
            }
        }
        stage('docker push') {
            steps {
               script {
                sh "docker push adrianyaniri/disenio-industrial:latest-${BUILD_NUMBER}"
               }
            }
        }
    }
}