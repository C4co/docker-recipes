#### Commands

Running a simple container
```
docker run -dti ubuntu
```

Access container interactive mode
```
docker exec -it container_name sh
```

Remove a docker container

```
docker rm --force container_name
```

Removing all containers
```
docker rm --force $(docker ps -a -q)
```

Log container
```
docker logs container name
```

Running a node container with ports and volume
```
docker run -dti -p 3000:3000 -v $(pwd):/app/ --name node-container node:18-alpine
```

Running Nginx

```
docker run -dti -p 2000:80 -v $(pwd):/usr/share/nginx/html --name nginx-container nginx
```

### Docker compose

Start containers
```
docker compose up -d
```

### Alias

Alias for shell


```
docker rm --force $(docker ps -a -q)
```

---

Carlos Costa @ 2022
