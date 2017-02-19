# docker-letsencrypt
letsencrypt in docker compose

```yaml
version: "3"

services:
 letsencrypt:
   image: jujiyangasli/letsencrypt
   volumes:
     - ./letsencrypt:/etc/letsencrypt
     - ./letsencrypt-bash:/letsencrypt-bash
   command: bash /letsencrypt-bash
```

use with nginx
```
    location /.well-known/acme-challenge {
    	proxy_pass http://<letsencrypt_host>:80;
    }
```
