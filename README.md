# alpine-certbot

#### [alpine-x64-certbot](https://hub.docker.com/r/forumi0721alpinex64/alpine-x64-certbot/)
![Docker Image Version (tag latest semver)](https://img.shields.io/docker/v/forumi0721alpinex64/alpine-x64-certbot/latest)
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/forumi0721alpinex64/alpine-x64-certbot/latest)
![MicroBadger Layers (tag)](https://img.shields.io/microbadger/layers/forumi0721alpinex64/alpine-x64-certbot/latest)
![Docker Pulls](https://img.shields.io/docker/pulls/forumi0721alpinex64/alpine-x64-certbot)
![Docker Stars](https://img.shields.io/docker/stars/forumi0721alpinex64/alpine-x64-certbot)
#### [alpine-aarch64-certbot](https://hub.docker.com/r/forumi0721alpineaarch64/alpine-aarch64-certbot/)
![Docker Image Version (tag latest semver)](https://img.shields.io/docker/v/forumi0721alpineaarch64/alpine-aarch64-certbot/latest)
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/forumi0721alpineaarch64/alpine-aarch64-certbot/latest)
![MicroBadger Layers (tag)](https://img.shields.io/microbadger/layers/forumi0721alpineaarch64/alpine-aarch64-certbot/latest)
![Docker Pulls](https://img.shields.io/docker/pulls/forumi0721alpineaarch64/alpine-aarch64-certbot)
![Docker Stars](https://img.shields.io/docker/stars/forumi0721alpineaarch64/alpine-aarch64-certbot)
#### [alpine-armhf-certbot](https://hub.docker.com/r/forumi0721alpinearmhf/alpine-armhf-certbot/)
![Docker Image Version (tag latest semver)](https://img.shields.io/docker/v/forumi0721alpinearmhf/alpine-armhf-certbot/latest)
![Docker Image Size (tag)](https://img.shields.io/docker/image-size/forumi0721alpinearmhf/alpine-armhf-certbot/latest)
![MicroBadger Layers (tag)](https://img.shields.io/microbadger/layers/forumi0721alpinearmhf/alpine-armhf-certbot/latest)
![Docker Pulls](https://img.shields.io/docker/pulls/forumi0721alpinearmhf/alpine-armhf-certbot)
![Docker Stars](https://img.shields.io/docker/stars/forumi0721alpinearmhf/alpine-armhf-certbot)



----------------------------------------
#### Description

* Distribution : [Alpine Linux](https://alpinelinux.org/)
* Architecture : x64,aarch64,armhf
* Appplication : [certbot](https://certbot.eff.org/)
    - Automatically enable HTTPS on your website with EFF's Certbot, deploying Let's Encrypt certificates.



----------------------------------------
#### Run

```sh
docker run -d \
           -p 80:80/tcp \
           -p 443:443/tcp \
           -v /repo:/repo \
           -e USER_EMAIL=<email> \
           -e CERT_DOMAIN=<domain,...> \
           forumi0721alpine[ARCH]/alpine-[ARCH]-certbot:latest
```

##### Notes
    - Certbot does not offer change ports, *You must set `-p 80:80/tcp -p 443:443/tcp`.* 



----------------------------------------
#### Usage

* Nothing to do.
    - It will automatically renew every 2 month. 
    - If you don't have letsencrypt yet, you should set USER_EMAIL and CERT_DOMAIN.
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

