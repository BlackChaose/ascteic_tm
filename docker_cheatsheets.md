# My cheatsheets for docker

***Show images***
```Docker
docker images -a
```
---
***Show images since one image***
```Docker

```
---

***Delete one image***
```Docker
docker image rm <imagename>
```
---
***Delete images by list***
```Docker
docker image rm -f $(docker images --format "{{.ID}}" )
```
---
***Delete all images***
```Docker
docker image prune
#or
docker image prune --all
```
---

***Delete all images with exclude some others [See documentation](https://docs.docker.com/engine/reference/commandline/image_prune/)***
```Docker
docker image prune -a --force --filter "until=2017-01-04T00:00:00"
#or
docker image prune --filter="label=deprecated"
#or
 docker image prune --filter="label!=maintainer=john"
```
---

***Delete all untagged images***
```Docker
docker rmi $(docker images -f "dangling=true" -q)
```
---

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

***Build from Dockerfile (Remember about target - for example "." if Dockerfile is in current directory!***
```Docker
docker build -t "<name>:<tag>" .
```
---

## My cheatsheets for docker-compose

***build and run docker containers using docker-compose***
```Docker
docker-compose up --build -d
```
---
***stop and delete containers, run in previous step***
```Docker
docker-compose rm -fs
```
---
