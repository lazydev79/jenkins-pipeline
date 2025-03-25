pipeline {
 agent any
 environment {
 DOCKER_USER = 'lazydev79'
 }
 stages {
 stage('Login Docker') {
 steps {
 withCredentials([string(credentialsId: 
'DOCKER_PASSWORD', variable: 'DOCKER_PASSWORD_SCOL')]) {
 sh 'echo $DOCKER_PASSWORD_SCOL | docker login -u $DOCKER_USER --password-stdin'
 }
 }
 }
 }
}
