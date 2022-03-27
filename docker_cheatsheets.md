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
