pipeline {
 agent any
 environment {
 DOCKER_USER = 'DOCKER_PASSWORD_SCOL'
 }
 stages {
 stage('Login Docker') {
 steps {
 withCredentials([string(credentialsId: 'DOCKER_PASSWORD', variable: 'DOCKER_PASS')]) {
 sh 'echo $DOCKER_PASS | docker login -u $DOCKER_USER --password-stdin'
 }
 }
 }
 }
}
