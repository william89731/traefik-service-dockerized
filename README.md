![20220327_120203](https://user-images.githubusercontent.com/68069659/160276555-e127963e-7bbf-4a5e-a9ab-3d3576bc5973.gif)
# traefik-service-dockerized

I wrote this guide to facilitate remote access with [traefik](https://traefik.io/), to various services:

[nodered](https://nodered.org/)

[homeassistant](https://www.home-assistant.io/)

[nextcloud](https://nextcloud.com/)

strongly recommend install [docker compose v2](https://docs.docker.com/compose/cli-command/) 

# step 1

create folders: 

mkdir /home/$USER/dockerDev/traefik/letsencrypt -p \ 
mkdir /home/$USER/dockerDev/homeassistant -p \
mkdir /home/$USER/dockerDev/nodered -p \
mkdir /home/$USER/dockerDev/nextcloud/data /home/$USER/dockerDev/nextcloud/appdata  /home/$USER/dockerDev/nextcloud/mysql  -p 

create files:

touch /home/$USER/dockerDev/.env  /home/$USER/dockerDev/docker-compose.yml

# step 2

copy:

[docker-compose.yml](https://github.com/william89731/traefik-service-dockerized/blob/master/docker-compose.yml) in your compose file

copy:

[env-example](https://github.com/william89731/traefik-service-dockerized/blob/master/env-example) in your .env file

navigate to your mother directory:

cd /home/$USER/dockerDev

and launch:

docker compose --env-file .env up  -d --remove-orphans

# credits

thanks to [danimart1191](https://github.com/danimart1991) for the inspiration to write this guide






