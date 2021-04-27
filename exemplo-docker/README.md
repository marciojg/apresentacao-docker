## hello world
- docker run hello-world

## Etapas
- docker build . -t devel/node-web-app
- docker images
- docker run -p 49160:8080 -d devel/node-web-app
- docker ps
- docker logs <container id / name>
- docker run devel/node-web-app pwd
- docker exec -it <container id / name> /bin/bash
- cat /etc/os-release
- curl -i localhost:49160
- docker run -p 123:8080 devel/node-web-app
- docker stop <container id / name>

## Extra

# docker rmi devel/node-web-app:latest

# WORKDIR /teste/plus
# RUN echo 'aaaa' > text.txt
# WORKDIR /usr/src/app
# docker build . -t devel/node-web-app
# docker run devel/node-web-app bash -c 'cat /teste/plus/text.txt'