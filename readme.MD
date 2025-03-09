# docker host newtork

Docker provides different networking modes, and one of them is host networking. When you use --network host, the container shares the same network namespace as the host, meaning:

✅ The container does not get its own IP address; instead, it uses the host’s IP.

✅ It bypasses Docker’s default bridge network, improving performance by reducing network overhead.

✅ It is mainly used when low latency and direct access to the host network are required.