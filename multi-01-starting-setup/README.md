# Run this demo

```console
docker network create <docker-network-name>  
```

```console
docker run -d --network <docker-network-name> --rm --name mongodb -v data:/data/db \
        -e MONGO_INITDB_ROOT_USERNAME=admin \
        -e MONGO_INITDB_ROOT_PASSWORD=secret \
        mongo
```

```console
docker run -d -p 3001:80 --name multi-back --rm -v logs:/app/logs -v "/path/to/project/backend:/app" -v /app/node_modules --network  <docker-network-name> <backend-image-name>:<backend-image-tag>
```

```console
docker run -p 3000:3000 -d --name multi-front --rm -it -v "/path/to/project/frontend/src:/app/src" --network <docker-network-name> -v /app/node_modules <frontend-image-name>:<frontend-image-tag>
```

## Docker Compose Commands

Some docker compose commands to start and stop the application

Start the application

```console
docker compose up
```

Start the application in detached mode

```console
docker compose up -d
```

Stop the application and remove the containers

```console
docker compose down
```

Stop the application removing the containers and the volumes

```console
docker compose down -v
```
