Manual de usuario
************************


Iniciar servidor
=================

Debemos primero posicionarnos en la carpeta build/src generada durante la instalacion
y utilizar el siguiente comando:

  > ./Appserver PUERTO DIRECCION_SHARED_SV LIMITE_CANDIDATOS

  PUERTO: Es el puerto local se reciben los requests de parte del cliente.

  DIRECCION_SHARED_SV: Es la URL del Shared Server.

.. warning:: La URL no debe incluir http o https. Por ejemplo: t2shared.herokuapp.com

  LIMITE_CANDIDATOS: Limite diario maximo de candidatos que puede pedir un usuario.

.. note:: Ejemplo: > ./Appserver 8000 t2shared.herokuapp.com 10



Cerrar el Servidor
====================

  En la carpeta donde se corre el servidor se encontrara un archivo llamado:
    comandos.txt

  Escribiendo: cerrar en una linea de este archivo se cerrara el server.



Cambiar el Shared
-------------------

  En la carpeta donde se corre el servidor se encontrara un archivo llamado:
    comandos.txt

  Escribiendo cambiarShared URL
  se cambiara la URL del sharedServer

  Ejemplo:

  cambiarShared t2shared.herokuapp.com



Docker
===========
