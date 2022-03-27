#My cheatsheets for Docker

***Delete all containers***
```Docker
docker rm -f $(docker ps -a -q)
```
---

***Delete all images*** [link to documentation](https://docs.docker.com/engine/reference/commandline/image_prune/)
```Docker
 docker image prune -a
```
---

***Publish port from container to host, for example use: http://localhost:5001 or use: http://localhost:10001***
```Docker
docker run -d -ti --publish 5001:5001 a02ecc649843
#or
docker run -ti -p 8080:10001 --name <container name> <name>:<tag>
            <container:host>
```
---

***Build from Dockerfile***
```Docker
docker build -t "<name>:<tag>" .
```
