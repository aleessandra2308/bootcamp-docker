MYSQL_ROOT_PASSWORD=1234567

MYSQL_DATABASE=docker-db

MYSQL_USER=docker-user

MYSQL_PASSWORD=12345

crear variables y correr contenedor
docker run -d -p 3306:3306 -e "MYSQL_ROOT_PASSWORD=1234567" -e "MYSQL_DATABASE=docker-db" -e "MYSQL_USER=docker-user" -e "MYSQL_PASSWORD=12345" mysql:5.7

Para ver si un contenedor se está autenticando
docker logs container_id

Conectarse a la bd con linea de comandos:
mysql -u root -h 127.0.0.1 -p1234567 --port 3306
