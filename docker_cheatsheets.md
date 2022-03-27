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

***Forward port from host to container***
```Docker
docker run -ti -p 8080:80 --name <container name> <name>:<tag>
            <container:host>
```
---

***Build from Dockerfile***
```Docker
docker build -t "<name>:<tag>" .
```
