# COMANDOS DE DOCKER                                                                                                                                                       



## Ver la version de Docker 
```
docker --version
```

## Crear un contenedor
```
docker create helloworld
```
o 
```
docker create helloworld:etiqueta
```

### Iniciar o arrancar un contenedor ya creado

```
docker start name
```

## Eliminar contenedores
```
docker rm ID_parcial
```
o 
```
docker rm ID
```
o 
```
docker rm name
```

### Eliminar un contenedor que esta corriendo

```
docker rm name -f
```

## Listar imagenes
```
docker images
```
o 
```
docker image ls
```

### Mostrar los contenedores que estan corriendo y los detenidos

```
docker ps
```

### Mostrar una lista de los contenedores que estan corriendo

```
docker stats --all
```

### Construir la imagen sin etiqueta

```
docker build 
```

### Construir la imagen con etiqueta

```
docker build -t helloworld:1.0
```

### Crear y comenzar un contenedor en una operacion 

```
docker run
```
## Crear contenedor y arrancarlo a la vez en segundo plano con un solo comando

```
docker run -d ...
```

## crear contenedor
```
docker run --name web01 -d -P helloworld
```

### Etiquetar la imagen como latest

```
docker tag helloworld:1.0 helloworld:latest
```

### Inspeccionar los metadatos de la imagen 

```
docker inspect helloworld:latest
```

### Mostrar el historial de una imagen

```
docker history
```

### Detener un contenedor

```
docker stop
```
### Pausar un contenedor

```
docker pause
```

### Quitar la pausa a un contenedor que esta corriendo 

```
docker unpause
```

## Extraer una imagen de Dockerhub(repositorio de docker)
```
docker pull httpd
```
## Obtener la ip de un contenedor desde inspect
```
docker inspect NAME|grep IPAddress
```
## Crear un contenedor publicando un puerto especifico

```
docker create -p 8080:80 --name web01 helloworld:latest
```

## Comprobar rango de puertos locales

```
cat /proc/sys/net/ipv4/ip_local_port_range
```                                                                          
 
 ## Algunos ejemplos de ejecutar comandos dentro del contenedor con exec
```
docker exec web01 ls /
docker exec web01 ps
```

## Ejecutar la shell bash dentro de un contenedor que esta corriendo
```
docker exec -it web01 bash
```

## Ver logs de nginx dentro del contenedor
```
tail -f /var/log/nginx/access.log
```
## Listar volumenes

```
docker volume ls
```

## Crear volumen
```
docker volume create my-volume
```

## Inspeccionar volumen
```
docker volume inspect my-volume
```

## Crear contenedor con volumen persistente
```
docker create -P --mount source=my-volume,target=/var/www/html --name web01 helloworld:latest
```

## Eliminar un volumen
```
docker volume rm my-volume
```

## Limpiar o purgar el listado de volumenes no utilizados
``` 
docker volume prune
```
## Listar redes

```
docker network ls
```

## Crear network

```
docker network create nombre_de_la_red --driver nombre_del_driver 
por ejemplo:
docker network create web --driver bridge
```

## Crear un contenedor dentro de una red

```
docker create --name web01 --network web helloworld
```

##  Filtrar ip en la salida de docker inspect
```
docker inspect web01 |grep IPAddress
```

## Eliminar las redes que no esten en uso

```
docker network prune
```

## Conectar y desconectar un contenedor de una red

```
docker connect web web01
docker disconnect web web01
```
                                                                          
                                                                         
