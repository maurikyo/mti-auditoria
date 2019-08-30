# Demo 1 - Sonarqube

[Fuente de la imagen](https://hub.docker.com/_/sonarqube/)  
[Más información](https://www.sonarqube.org/)

## Obtener la imagen desde la red local

~~~ bash
docker pull IP:5000/demo1sonar
~~~

## Generar el contenedor

~~~ bash
docker run -d --name sonarqube -p 9000:9000 demo1sonar
~~~

## Consideraciones previas

Se va a analizar un proyecto de muestra con código Python / PHP. El mismo se encuentra en la carpeta **codigo**.

## Pasos a seguir

1. Ingresar en el navegador a la [aplicación](http://localhost:9000/)
2. Login con las credenciales por defecto **admin : admin**
3. Generar un nuevo proyecto:
    + Definir un nombre
    + Generar un token
    + Seleccionar lenguaje y sistema operativo (SO)
    + Descomprimir la versión correspondiente a su SO del **sonar-scanner** que se encuentra comprimido en esta misma carpeta
4. Ejecutar sonar-scanner en la carpeta donde se encuentre el código fuente a analizar
5. Una vez que termine la ejecución, volver al navegador y ver los resultados del proyecto
6. Generar el reporte del uso de la herramienta para el registro de las evidencias que se encuentren

## Origen del código a analizar

[Repositorio](https://github.com/genack/gPOS)

## Apagado del contenedor

~~~ bash
docker stop sonarqube
~~~
