### Docker images
_Mostrar listado de todas las imagenes
'docker images'

### Docker ps
_docker ps muestra el listado de los contenedores en ejecución
'docker ps'

### Docker Pull
_docker pull permite extraer la imagen de un repositorio
'docker pull'

### Docker Push
par docker hub

### Docker run
_Iniciar el contenedor
docker run

### Docker exec
_docker exec para conectarse y obtener una shell
docker exec -ti CONTENEDOR_ID

### Docker inspect
comando que permite obtener información detallada del contenedor

### Docker rm
comando para eliminar contenedores, imágenes, volumenes
'docker rm -f contenedor_id'

### Iniciar | Detener | Reiniciar
docker start contenedor_id
docker stop contenedor_id

### Ejemplo


### Mapear puerto para levantar una imagen
docker run -d -p 8080:8080 jenkins/jenkins:latest
### Entrar al contenedor con bash
docker exec -ti 6bea4a6b15e6 bash
### Ubicar la ruta donde esta el secret de jenkins para hacer un cat (esto ya dentro del contenedor con bash)
cat /var/jenkins_home/secrets/initialAdminPassword
### Salir del contenedor
exit
### Agregar usuario root a un contenedor
docker exec -u root -ti 'container_id' bash
### Variables de entorno
Se agrega al correr el contenedor
docker run -d -e 'prueba1=4321' nathanpeck/greeting
Entrar al contenedor a revisar si tiene variables de entorno:
Ver todas las variables de entorno: printenv
Ver una variable en estecifico: echo $prueba1


