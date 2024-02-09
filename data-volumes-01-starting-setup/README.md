# Run with Volumes

To run this code use the command:

```console
docker run -p 3000:8000 --env PORT=8000 -d --name feedback-app-volume --rm -v feedback:/app/feedback -v "/path/to/code:/app:ro" -v /app/temp -v /app/node_modules <image-name>:<image-tag>
```
