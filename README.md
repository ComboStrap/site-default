# ComboStrap Default Installation WebSite


## About

This is the default [ComboStrap Website](https://combostrap.com/admin/combostrap-website-5gxpcdgy) 
that is installed by [ComboStrap DokuWiki Docker](https://combostrap.com/admin/dokuwiki-docker-9iq3aso8)


## How to run

On your desktop:

```bash
git clone 
cd site-default
docker run \
  --name combo-site-default \
  --rm \
  -p 8081:80 \
  -e DOKU_DOCKER_GIT=https://github.com/ComboStrap/site-default \
  ghcr.io/combostrap/dokuwiki:php8.3-v1
```
The default ComboStrap site should be available at: http://localhost:8081


## How to develop or contribute

See [How to develop or contribute](docs/dev.md)
