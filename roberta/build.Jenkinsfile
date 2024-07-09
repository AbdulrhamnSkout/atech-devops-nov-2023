pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'printenv'
                sh 'docker login -u abd0525656@gmail.com -p ${DOCKER_PASS}'
                sh 'docker build -t abdskcot/jenkins_test_repo:${env.BUILD_NUMBER} '
                sh 'docker push abdskcot/jenkins_test_repo:${env.BUILD_NUMBER} '
            }
        }
    }
}