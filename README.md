# DOCKER
COMANDOS DE DOCKER
## Comandos

## Ver la version de Docker 
```
docker --version
```
## Extraer una imagen de Dockerhub(repositorio de docker)
```
docker pull httpd
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

### Etiquetar la imagen como latest

```
docker tag helloworld:1.0 helloworld:latest
```

### Inspeccionar los metadatos de la imagen 

```
docker inspect helloworld:latest
```

### Crear y comenzar un contenedor en una operacion 

```
docker run
```

### Borrar una imagen

```
docker rmi 
```

### Mostrar el historial de una imagen

```
docker history
```
