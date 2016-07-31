docker build -t chatserver .  ;
docker run -d --name jenkins -p 8080:8080 -v /var/run/docker.sock:/var/run/docker.sock chatserver



Running these would create Jenkins container and inside jenkins container would run all other application images
Open page of Jenkins Container and target repository https://github.com/MuhammadSuhail/chatServerDocker. Then open Batch of jenkins and add jenkins_shell file code in it. 
Whenevr there is a change in code on https://github.com/MuhammadSuhail/chatServerDocker the jenkins would get triggered and run the bash scripts and if succeded would push the docker images on the dockerhub.

You can control the environment from https://github.com/MuhammadSuhail/chatServerDocker docker-compose file
