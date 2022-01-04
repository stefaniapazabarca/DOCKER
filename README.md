# COMANDOS DE DOCKER                                                                                                                                                       



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

### Crear y comenzar un contenedor en una operacion 

```
docker run
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

### Borrar una imagen

```
docker rmi 
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

                                                                          
                                                                          
                                                                          
                                                                         
