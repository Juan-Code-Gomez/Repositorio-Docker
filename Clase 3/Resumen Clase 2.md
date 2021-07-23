# **Resumen Clase 3**
## _The Last Markdown Editor, Ever_

En la clase 3 vimos lo relacionado con imagenes y contenedores en docker

- Dfinicion e introduccion
- Ejemplos 
- Y practica

## Definicion

Se entiende por imagen como plantilla de instrucciones para la creacion de un contenedor
Para crear imagenes propias se realizan con los comandos de DockerFile y ejecutarla

Se entiende por contenedores como una instancia ejecutable de la imagen, la cual se puede crear, iniciar, detener y eliminar por medio de comandos


## Practica

Para crear una imagen debemos seguir los siguientes pasos:

- Creamos una carpeta donde correra el contenedor
-  Dentro de la carpeta se ejecuta el comando vim dockerfile
-  Despues de ejecutar el comando, ingresamos i, para insertar la imagen
- y luego insertamos la siguiente imagen  ```shdocker image build -t some-content-nginx .```
- Y presionamos escape, y escribimos :wq para salir.



Una vez insertada la imagen, creamos otra carpeta dentro del directorio en el que estamos, y dentro insertamos el mensaje que contendra la imagen
Luego salimos y corremos la imagen
```sh
docker run --name some-nginx -d -p 8080:80 some-content-nginx
```


