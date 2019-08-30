# Demo 2 - Python + Jupyter + Pandas

[Fuente de la imagen](https://hub.docker.com/r/owasp/zap2docker-stable)  
[Documentación](https://github.com/zaproxy/zaproxy/wiki/Docker)  
[Ejecución en el navegador](https://github.com/zaproxy/zaproxy/wiki/WebSwing)

## Obtener la imagen desde la red local

~~~ bash
docker pull 172.16.7.200:5000/demo3owasp
~~~

## Generar el contenedor

~~~ bash
docker run -u zap -p 8080:8080 -p 8090:8090 -i 172.16.7.200:5000/demo3owasp zap-webswing.sh
~~~

**Recomendación:** no es conveniente ejecutar este tipo de análisis sobre un sitio en producción sin avisar al auditado. Aunque también puede servir para determinar las medidas de seguridad que se hayan tomado para prevenir este tipo de análsis.

## Pasos a seguir

1. Cuando inicia el contenedor se va a abrir una interfaz en el navegador web
2. Desde la pantalla de "Quick Start" se puede comenzar un ataque a un sitio web específico.
3. Una vez que la herramienta realiza el análsis produce un conjunto de salidas que se pueden revisar, puntualmente en la pestaña de "Alerts" en la sección inferior de la pantalla
4. El reporte generado puede ser exportado a HTML y guardado como resultado de la ejecución. Sus resultados deberán ser evaluados. De corresponder, registrar las evidencias para la confección posterior de los hallazgos

## Apagado del contenedor

~~~ bash
Ctrl + C
~~~
