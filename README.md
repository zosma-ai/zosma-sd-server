# zosma-sd-server
Task Queue Manager for distributed Stable Diffusion Worker network based on [asynq](https://github.com/hibiken/asynq) and [redis](https://github.com/redis/redis).

Worker is created by integrating workers/worker with [Stable Diffusion WebUI API](https://github.com/AUTOMATIC1111/stable-diffusion-webui)

Client applications, for example [zosma-discord-bot](https://github.com/rampenke/zosma-discord-bot) uses clinet interface as shown in the example clients/client.go 

## Build
```
docker build -t zosma-sd-webserver -f Dockerfile.webserver .
docker build -t zosma-sd-workershim -f Dockerfile.workershim .
```
## local testing

```
docker run -it --rm --env-file .env -p 1324:1324 zosma-sd-webserver
```