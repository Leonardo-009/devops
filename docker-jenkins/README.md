### docker-jenkins

### docker build -t jenkins:latest .

### docker run -d --name jenkins -p 8080:8080 jenkins:latest

### http://localhost:8080

# user o comando abaixo para consegui o password do ambiente jenkins atraves da imagem docontainer_id

### docker exec -it <container_id> cat /var/jenkins_home/secrets/initialAdminPassword