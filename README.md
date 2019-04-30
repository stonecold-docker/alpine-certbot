# alpine-certbot

#### [alpine-x64-certbot](https://hub.docker.com/r/forumi0721alpinex64/alpine-x64-certbot/)
[![](https://images.microbadger.com/badges/version/forumi0721alpinex64/alpine-x64-certbot.svg)](https://microbadger.com/images/forumi0721alpinex64/alpine-x64-certbot "Get your own version badge on microbadger.com") [![](https://images.microbadger.com/badges/image/forumi0721alpinex64/alpine-x64-certbot.svg)](https://microbadger.com/images/forumi0721alpinex64/alpine-x64-certbot "Get your own image badge on microbadger.com") [![Docker Stars](https://img.shields.io/docker/stars/forumi0721alpinex64/alpine-x64-certbot.svg?style=flat-square)](https://hub.docker.com/r/forumi0721alpinex64/alpine-x64-certbot/) [![Docker Pulls](https://img.shields.io/docker/pulls/forumi0721alpinex64/alpine-x64-certbot.svg?style=flat-square)](https://hub.docker.com/r/forumi0721alpinex64/alpine-x64-certbot/)
#### [alpine-aarch64-certbot](https://hub.docker.com/r/forumi0721alpineaarch64/alpine-aarch64-certbot/)
[![](https://images.microbadger.com/badges/version/forumi0721alpineaarch64/alpine-aarch64-certbot.svg)](https://microbadger.com/images/forumi0721alpineaarch64/alpine-aarch64-certbot "Get your own version badge on microbadger.com") [![](https://images.microbadger.com/badges/image/forumi0721alpineaarch64/alpine-aarch64-certbot.svg)](https://microbadger.com/images/forumi0721alpineaarch64/alpine-aarch64-certbot "Get your own image badge on microbadger.com") [![Docker Stars](https://img.shields.io/docker/stars/forumi0721alpineaarch64/alpine-aarch64-certbot.svg?style=flat-square)](https://hub.docker.com/r/forumi0721alpineaarch64/alpine-aarch64-certbot/) [![Docker Pulls](https://img.shields.io/docker/pulls/forumi0721alpineaarch64/alpine-aarch64-certbot.svg?style=flat-square)](https://hub.docker.com/r/forumi0721alpineaarch64/alpine-aarch64-certbot/)
#### [alpine-armhf-certbot](https://hub.docker.com/r/forumi0721alpinearmhf/alpine-armhf-certbot/)
[![](https://images.microbadger.com/badges/version/forumi0721alpinearmhf/alpine-armhf-certbot.svg)](https://microbadger.com/images/forumi0721alpinearmhf/alpine-armhf-certbot "Get your own version badge on microbadger.com") [![](https://images.microbadger.com/badges/image/forumi0721alpinearmhf/alpine-armhf-certbot.svg)](https://microbadger.com/images/forumi0721alpinearmhf/alpine-armhf-certbot "Get your own image badge on microbadger.com") [![Docker Stars](https://img.shields.io/docker/stars/forumi0721alpinearmhf/alpine-armhf-certbot.svg?style=flat-square)](https://hub.docker.com/r/forumi0721alpinearmhf/alpine-armhf-certbot/) [![Docker Pulls](https://img.shields.io/docker/pulls/forumi0721alpinearmhf/alpine-armhf-certbot.svg?style=flat-square)](https://hub.docker.com/r/forumi0721alpinearmhf/alpine-armhf-certbot/)



----------------------------------------
#### Description

* Distribution : [Alpine Linux](https://alpinelinux.org/)
* Architecture : x64,aarch64,armhf
* Appplication : [certbot](https://certbot.eff.org/)
    - Automatically enable HTTPS on your website with EFF's Certbot, deploying Let's Encrypt certificates.
* Base Image
    - [forumi0721/alpine-x64-base](https://hub.docker.com/r/forumi0721/alpine-x64-base/)
    - [forumi0721/alpine-aarch64-base](https://hub.docker.com/r/forumi0721/alpine-aarch64-base/)
    - [forumi0721/alpine-armhf-base](https://hub.docker.com/r/forumi0721/alpine-armhf-base/)



----------------------------------------
#### Run
* x64
```sh
docker run -d \
           -p 80:80/tcp \
           -p 443:443/tcp \
           -v /repo:/repo \
           -e USER_EMAIL=<email> \
           -e CERT_DOMAIN=<domain,...> \
           forumi0721alpinex64/alpine-x64-certbot:latest
```

* aarch64
```sh
docker run -d \
           -p 80:80/tcp \
           -p 443:443/tcp \
           -v /repo:/repo \
           -e USER_EMAIL=<email> \
           -e CERT_DOMAIN=<domain,...> \
           forumi0721alpineaarch64/alpine-aarch64-certbot:latest
```

* armhf
```sh
docker run -d \
           -p 80:80/tcp \
           -p 443:443/tcp \
           -v /repo:/repo \
           -e USER_EMAIL=<email> \
           -e CERT_DOMAIN=<domain,...> \
           forumi0721alpinearmhf/alpine-armhf-certbot:latest
```

##### Notes
* Certbot does not offer change ports, *You must set `-p 80:80/tcp -p 443:443/tcp`.* 



----------------------------------------
#### Usage

* Nothing to do.
    - It will automatically renew every 2 month. 

##### Notes
    -  If you don't have letsencrypt yet, you should set USER_EMAIL and CERT_DOMAIN.
       Also you need to mount /repo (Because cert file generate in docker container)



----------------------------------------
#### Docker Options

| Option             | Description                                      |
|--------------------|--------------------------------------------------|
| -                  | -                                                |


#### Ports

| Port               | Description                                      |
|--------------------|--------------------------------------------------|
| 80/tcp             | HTTP port                                        |
| 443/tcp            | HTTPS port                                       |


#### Volumes

| Volume             | Description                                      |
|--------------------|--------------------------------------------------|
| /repo              | Persistent data                                  |


#### Environment Variables

| ENV                | Description                                      |
|--------------------|--------------------------------------------------|
| USER_EMAIL         | Cert email (If you already have cert, it does not need.)  |
| CERT_DOMAIN        | Cert domian (If you already have cert, it does not need.) |



----------------------------------------
* [forumi0721alpinex64/alpine-x64-certbot](https://hub.docker.com/r/forumi0721alpinex64/alpine-x64-certbot/)
* [forumi0721alpinearmhf/alpine-armhf-certbot](https://hub.docker.com/r/forumi0721alpinearmhf/alpine-armhf-certbot/)
* [forumi0721alpineaarch64/alpine-aarch64-certbot](https://hub.docker.com/r/forumi0721alpineaarch64/alpine-aarch64-certbot/)

