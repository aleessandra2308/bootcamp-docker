docker run -d --name apache -p 80:80 httpd

crear un index y agregarle datos (primero ubicarse en la carpeta)
echo "HOLAAAA" > index.html

Para copiar archivos de un contenedor a otro
docker cp nombre_archivo origen:destino
docker cp index.html apache:/tmp

entrar comando sh
docker exec -it apache sh
