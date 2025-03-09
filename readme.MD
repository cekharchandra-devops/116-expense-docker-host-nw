# docker host newtork

Docker provides different networking modes, and one of them is host networking. When you use --network host, the container shares the same network namespace as the host, meaning:

✅ The container does not get its own IP address; instead, it uses the host’s IP.

✅ It bypasses Docker’s default bridge network, improving performance by reducing network overhead.

✅ It is mainly used when low latency and direct access to the host network are required.



![alt text](image.png)

if you notice Networks section, host network doesnt assign IP address.

instead of using IP address or container name, we have to mention localhost for container to container communication.

commands to deploy services:

```
 docker run -d --name mysql --network host mysql:v1
 docker run -d --name backend --network host backend:v1
 docker run -d -p 80:80 --name frontend --network host frontend:v1
```