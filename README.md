# ComboStrap Default WebSite


## About

This is the default website that is installed with `dokuwiki docker`



## How to run

```bash
git clone https://github.com/ComboStrap/site-default
cd site-default
docker run \
  --name combo-site-default \
  --rm \
  -p 8081:80 \
  -e DOKU_DOCKER_ENV=dev \
  -v $PWD:/var/www/html \
  ghcr.io/combostrap/dokuwiki:php8.3-v1
```
The default ComboStrap site should be available at: http://localhost:8081 