# **Resumen Clase 4**
## _The Last Markdown Editor, Ever_

En la clase 4 vimos como sincronizar docker con jenkins.

- Dfinicion e introduccion


## Definicion

Jenkins es un servidor de integracion continua y es gratuito, junto con docker podemos desplegar la aplicacion y en jenkins realizar la integracion continua para realizar pruevas o el versionamiento o notificaciones de algun error

Por otro lado Docker permite construir de forma rapida y estanderizadas las aplicaciones
y compartirlas.

Son aplicaciones en su propio contenedor, sin importar cuantos
contenedores podemos tener activos.

## Practica

Para sincronizar el contenedor con jenkins:

- Creamos una carpeta donde correra el contenedor
-  Dentro de la carpeta se ejecuta el comando vim dockerfile
-  Despues ejecutamos el comando
 ```sh
docker-compose -f docker-compose-jenkins.yml up -d
```
- Luego nos pide el usuario y lo ingresamos  ```sudo chown ubuntu:ubuntu jenkins_home/ .```
despues de darle permisos de ejecuccion le damos el comando
 ```sh
docker logs -f jenkins
```

Luego ingresamos a la url e ingresamos a jenkins con el usuario e instalamos los componentes requeridos.





