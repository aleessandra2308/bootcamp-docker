### DOCKER VOLUMES
Permite que los datos queden persistentes en el contenedor

-e -> indicar variables de entorno en docker
-v -> variables de entorno en los volumenes

docker run -v nombre_volumen:/var/lib/mysql mysql:5.7

### Eliminar volumenes
docker volume rm nombre-volumen

### Listar volumenes
docker volume ls

### Creando un volumen
docker run -d -it --name test-container -v "bootVolume":/tmp ubuntu:xenial

/usr/share/nginx/html/
### Para que persista el archivo index de docker-2
docker run -v $PWD/index.html:/usr/share/ngnix/html/index.html -d -p 81:80 nginx
-d -> para que se haga en 2do plano

### Docker networking
app     <--->    bd

bridge
host
none

docker network ls

docker inspect network_id
para filtrar solo los host
docker inspect network_id |grep host

