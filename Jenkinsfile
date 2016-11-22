node('baremetal0') {
   stage('Checkout') {
       checkout scm
   }
   stage('Build docker image') {
       sh "docker build -t ccp/jenkins-docker-build-slave ."
   }
   stage('Publish image') {
       sh "docker push localhost:31500/ccp/jenkins-docker-build-slave"
   }
}
