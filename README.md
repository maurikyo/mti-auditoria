# Seguridad y Auditoría Informática - MTI 2019

## Introducción

Repositorio con el contenido necesario para el desarrollo de las actividades prácticas correspondientes a la temática **CAATs** de la asignatura.

## Consideraciones sobre el entorno de trabajo

Se va a utilizar docker en la **red local** [[REF]](https://docs.docker.com/registry/), considerando que está instalado en cada equipo se debe copiar el archivo *daemon.json* de la raíz de este repositorio a la ubicación correspondiente a su sistema operativo. [[REF]](https://docs.docker.com/registry/insecure/).

Para el caso de windows:

* C:\ProgramData\docker\config\daemon.json
* Desde la aplicación de gestión de Docker Desktop en **Settings > Daemon** agregar ahí la IP:5000 del repositorio de imágenes de la red

Para el caso de Linux:

* /etc/docker/daemon.json

Una vez hecho esto, se debe **reiniciar** el servicio docker en el equipo.

## Descarga de todas las imágenes a utilizar

~~~ bash
docker pull IP:5000/demo1sonar
docker pull IP:5000/demo2python
docker pull IP:5000/demo3owasp
~~~

## Presentaciones y materiales usados en clase

En el archivo **Archivos-Clase-CAATs.zip** se encuentran la presentación utilizada en clase, el documento del TP a presentar y el documento modelo para documentar el uso de CAATs en un proyecto de auditoría.
