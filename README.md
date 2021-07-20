# alpine-certbot
![Docker Pulls](https://img.shields.io/docker/pulls/forumi0721alpinex64/alpine-x64-certbot)
![Docker Stars](https://img.shields.io/docker/stars/forumi0721alpinex64/alpine-x64-certbot)

#### x86_64
![Docker Image Version](https://img.shields.io/docker/v/forumi0721alpinex64/alpine-certbot/latest)
![Docker Image Size](https://img.shields.io/docker/image-size/forumi0721alpinex64/alpine-certbot/latest)
#### aarch64
![Docker Image Version](https://img.shields.io/docker/v/forumi0721alpineaarch64/alpine-gcertbot/aarch64)
![Docker Image Size](https://img.shields.io/docker/image-size/forumi0721alpineaarch64/alpine-gcertbot/aarch64)



----------------------------------------
#### Description

* Distribution : [Alpine Linux](https://alpinelinux.org/)
* Architecture : x64,aarch64
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
           forumi0721/alpine-certbot:[ARCH_TAG]
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

