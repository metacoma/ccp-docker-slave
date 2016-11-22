node('baremetal0') {
   stage('Checkout') {
       checkout scm
   }
   stage('Build docker image') {
       sh "docker build -t ccp/jenkins-docker-build-slave ."
   }
}
