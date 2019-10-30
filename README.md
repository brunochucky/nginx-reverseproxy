## NGINX Reverse Proxy HTTPS

## 1. pull
docker pull brunosou/reverse_proxy

## 2. build
docker build -t brunosou/reverse_proxy .

## 3. run
docker run -p 443:443 --env-file ./env.dev -it $(docker build -q .) /bin/sh -c "nginx"

## 4. Browse
http://localhost/

## Source: Docker config for a very small nginx container
https://github.com/cybercode/alpine-nginx