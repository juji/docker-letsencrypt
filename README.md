# docker-letsencrypt
letsencrypt in docker compose

```
version: "3"

services:
 letsencrypt:
   image: jujiyangasli/letsencrypt
   volumes:
     - ./letsencrypt:/etc/letsencrypt
     - ./letsencrypt-bash:/letsencrypt-bash
   command: bash /letsencrypt-bash
```
