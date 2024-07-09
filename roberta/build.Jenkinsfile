pipeline {
    agent any
     environment {
            DOCKER_PASS = credentials('docker-hub')
        }
    stages {
        stage('Build') {
            steps {
                sh 'printenv'
                sh "docker login -u abdskcot -p ${env.DOCKER_PASS}"
                sh 'ls'
                dir('roberta'){
                sh "docker build -t abdskcot/jenkins_test_repo:${env.BUILD_NUMBER} ."
                sh "docker push abdskcot/jenkins_test_repo:${env.BUILD_NUMBER}"
            }
          }
        }

    }
}