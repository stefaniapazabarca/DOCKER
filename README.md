# DOCKER
COMANDOS DE DOCKER
## Comandos

## Listar imagenes
```
docker images
```
o 
```
docker image ls
```

### construir la imagen sin etiqueta

```
docker build 
```

### construir la imagen con etiqueta

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
