---
layout: post
title:  "Membuat sendiri code server"
date:   2023-12-23 20:29:00 +0200
category: tutorials
---

# ![image](https://github.com/py7hon/web/assets/29944979/75fc4796-1983-4094-bbd6-938ebc6bca3c)

Disini saya akan membagikan tentang cara membuat code-server pada server atau pc sendiri.

Langsung saja tanpa basa basi kita lakukan caranya.

## Install code-server

Disini yang kita butuhkan adalah Docker dan vim atau Nano utuk Editor text nya.

1. Buatlah sebuah folder yang bernama code-server

```terminal
$ mkdir code-server
```

2. Buka folder code-server

```
$ cd code-server
```

3. Buatlah sebuah file dengan bernama docker-compose.yml

```
$ nano docker-compose.yml
```

4. Jika sudah terbuka Nano atau Vim kalian bisa copy code YAML di bawah ini

```yaml
version: "3.7"
services:
  code-server:
    image: codercom/code-server:latest
    container_name: code-server
    environment:
      - DOCKER_USER=$USER
      - PASSWORD=sebuahpasswordyangsangatkuat #Ganti Password untuk login
    volumes:
      - ./config:/config
      - $PWD:/home/coder/workspace
    ports:
      - 8080:8080
    restart: unless-stopped
    networks:
    - code-server
```

5. Jika sudah di copy kalian bisa edit terlebih dahulu atau bisa langsung save.

6. Apa bila sudah di save kalian bisa langsung install dan compose.

```
$ docker compose up -d
```

7. Jika sudah di compose kalian bisa membuka nya pada localhost:8080 atau juga bisa di buat vhost pada nginx

```
server {
    listen 80;
    listen [::]:80;

    server_name code.iqbalrifai.eu.org;

    location / {
        proxy_pass http://localhost:8080;
    }
}
```

8. Dan jika sudah dibuat kalian bisa membuka nya contoh [https://code.iqbalrifai.eu.org](https://code.iqbalrifai.eu.org) (Private)

9. Dan kalian sudah berhasil menginstall code-server.