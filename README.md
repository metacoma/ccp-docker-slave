```bash
docker build -t localhost:3150/ccp/docker-build-slave .
docker push localhost:31500/ccp-pipeline/docker-build-slave
docker run -d -v /var/run/docker.sock:/var/run/docker.sock -p 0.0.0.0:4422:22 localhost:31500/ccp-pipeline/jenkins-slave
```
