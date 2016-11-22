node('baremetal0') {
   stage('Checkout') {
       checkout scm
   }
   stage('Build docker image') {
      sh "docker build -t ${env.REGISTRY_URL}/ccp/jenkins-docker-build-slave ."
   }
   stage('Publish image') {
      sh "docker push ${env.REGISTRY_URL}/ccp/jenkins-docker-build-slave"
   }
}
