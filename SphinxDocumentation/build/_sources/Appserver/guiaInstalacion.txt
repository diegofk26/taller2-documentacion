Guia de instalacion
************************

Descarga
===========

Para descargar este servidor se debera ir al `repositorio del proyecto <https://github.com/seguijoaquin/taller2-appserver>`_
o bien utilizando el siguiente comando:

  > git clone https://github.com/seguijoaquin/taller2-appserver.git


Dependencias
===========

Base de datos RocksDB, Framework de testing Google tests, junto con Google Mock para instalarlos:

  > ./instalar_dependencias.sh

Se utiliza mongoose para la parte de web server; no es necesaria su instalacion.

Se utiliza jsoncpp como parser; no es necesaria su instalacion previa.


Instalacion
===========

Se detallaran los pasos a seguir para instalar el servidor en ubuntu 14.04 y por consola,
ante algun error causado por utilizar otro sistema, utilizarlo mediante Docker.

Posicionarse en la carpeta del proyecto, es decir, aquella que fue creada ante
la invocacion del comando git clone. Una vez ahi invocar los siguientes comandos de bash:

  > mkdir -p build

  > cd build

  > cmake ..

  > make


Instalacion de Docker
=====================

1. Obtener docker desde la `pagina oficial de docker <https://www.docker.com/>`_

2. Si es la primera vez que se quiere ejecutar el Contenedor. Ejecutar el siguiente comando:

  > sudo docker sudo docker run -i -t -p 8000:8000 juanmafc/app_server:v1

.. warning:: Esto mapea el puerto 8000 del host al puerto 8000 del contenedor para mas informacion sobre como se puede cambiar estos puertos ver el manual de usuario en la seccion de Docker.
