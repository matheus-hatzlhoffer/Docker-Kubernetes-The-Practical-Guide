# Run this demo

```console
docker network create <docker-network-name>    
docker run -d --name mongodb --network <docker-network-name> mongo  
docker run --name favorite -d --rm -p 3000:3000 --network <docker-network-name> <image-name>:<image-tag>
```
