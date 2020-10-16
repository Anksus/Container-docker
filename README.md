# Container-docker
Notes on Container

link for Brian Holt notes
> https://btholt.github.io/complete-intro-to-containers/



### Basics

To know which OS version of host 
```
cat /etc/issue 
``` 


To run container 
```
docker run --interactive --tty alpine:3.10
``` 
short-ver
```
docker run -it alpine:3.10
```
-it -> for interactive shell

To run container in the background 
```
docker run --detach -it ubuntu:bionic
```  
short-ver 
```
docker run -dit ubuntu:bionic
```

To show running container which docker is managing for us
``` 
docker ps --all 
``` 



To kill a container running in the background
``` 
docker kill name_container 
```

To name a conatiner use this flag
```
--name
```
To kill it automatically after exiting use this flag
```
--rm 
```

example -- 
```
docker run --rm -dit --name my-ubuntu ubuntu:bionic
```

To remove containers and images
``` 
docker container prune || docker image prune
```


To fetch container for running
``` 
docker pull jturpin/hollywood 
```
(`push` is used to push container to registry like docker hub)

To know more about container
```
docker inspect node
```

To pauses or unpause all the processes in a container
```
docker pause <ID or name> || docker unpause <ID or name>
```
To execute commands against running container
```
docker exec <ID or name> <command (like-ps aux)>
```

To know overall history of composition of container 
```
docker history node
```

To know more about the host system
```
docker info
```
To know processes running in the container
```
docker run mongo
docker top <ID outputted by previous command> # you should see MongoDB running
```
To see Logs
```
docker log mongo
```
Restart - (it restarts)

To search into registry
```
docker search python
```