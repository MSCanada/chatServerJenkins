docker build -t chatserver .  ;
docker run -d --name jenkins -p 8080:8080 -v /var/run/docker.sock:/var/run/docker.sock chatserver
