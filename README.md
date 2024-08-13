# ComboStrap Default Installation WebSite


## About

This is the default [ComboStrap Website](https://combostrap.com/admin/combostrap-website-5gxpcdgy) 
that is installed by [ComboStrap DokuWiki Docker](https://combostrap.com/admin/dokuwiki-docker-9iq3aso8)


## How to get this website in readonly mode

To get this website:
* available at: http://localhost:8081 on your desktop
* in read only mode (read for everyone, write and upload for no one)

run:
```bash
docker run \
  --name combo-site-default \
  --rm \
  -p 8081:80 \
  -e DOKU_DOCKER_GIT_SITE='https://github.com/ComboStrap/site-default' \
  ghcr.io/combostrap/dokuwiki:php8.3-v1
```


## How to get this website with an admin user 

To get this website:
* available at: http://localhost:8081 on your desktop
* with an `admin` user (password: `welcome`)
* in `public` ACL policy (read for everyone, write and upload for registered users)

```bash
docker run \
  --name combo-site-default \
  --rm \
  -p 8081:80 \
  -e DOKU_DOCKER_ACL_POLICY='public' \
  -e DOKU_DOCKER_ADMIN_NAME='admin' \
  -e DOKU_DOCKER_ADMIN_PASSWORD='welcome' \
  -e DOKU_DOCKER_GIT_SITE='https://github.com/ComboStrap/site-default' \
  ghcr.io/combostrap/dokuwiki:php8.3-v1
```



## How to develop or contribute

See [How to develop or contribute](docs/dev.md)



