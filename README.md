## 👋 Welcome to tor-browser 🚀  

   
  
  
## Requires scripts to be installed  

```shell
 sudo bash -c "$(curl -q -LSsf "https://github.com/systemmgr/installer/raw/main/install.sh")"
 systemmgr --config && systemmgr install scripts  
```

## Automatic install/update  

```shell
dockermgr update tor-browser
```

## via command line  

```shell
docker pull casjaysdevdocker/tor-browser:latest && \
docker run -d --name tor-browser \
-ti --rm --net host -e DISPLAY \
-v /tmp/.X11-unix:/tmp/.X11-unix \
-v $HOME/.Xauthority:/home/x11user/.Xauthority \
casjaysdevdocker/tor-browser $@
```

## via docker-compose  

```yaml
version: "2"
services:
  tor-browser:
    image: casjaysdevdocker/tor-browser
    container_name: tor-browser
    environment:
      - TZ=America/New_York
      - HOSTNAME=casjaysdev-tor-browser
    volumes:
      - $HOME/.local/share/srv/docker/tor-browser/dataDir/data:/data:z
      - $HOME/.local/share/srv/docker/tor-browser/dataDir/config:/config:z
    ports:
      - 80:80
    restart: always
```

## Author  

🤖 casjay: [Github](https://github.com/casjay) [Docker](https://hub.docker.com/r/casjay) 🤖  
📽  dockermgr: [Github](https://github.com/dockermgr) [Docker](https://hub.docker.com/r/dockermgr) 📽  
⛵ CasjaysDev Docker: [Github](https://github.com/casjaysdevdocker) [Docker](https://hub.docker.com/r/casjaysdevdocker) ⛵  
