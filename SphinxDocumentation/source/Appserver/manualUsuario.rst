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

  Para utilizar el servidor en un contenedor se deben seguir los siguientes
  pasos:

  1. Pararse en la carpeta Docker del proyecto.
  2. Utilizar el siguiente comando:

    > docker build -t appserver .

  3. Correr el container con:

    > docker run -i -t --name appserver -e PUERTO='3000' -e SHARED_DIR='direccion del shared' -e LIMITE_CANDIDATOS='numero entero positivo' -p 8000:3000 appserver

    Donde se deben completar:

      PUERTO='Puerto del App server', el cual debe ser el mismo que el segundo puerto
      de -p PUERTO_HOST:PUERTO_APP

      SHARED_DIR: Es la URL del Shared Server.

      .. warning:: La URL no debe incluir http o https. Por ejemplo: t2shared.herokuapp.com

      LIMITE_CANDIDATOS: Limite diario maximo de candidatos que puede pedir un usuario.


    4. Para cerrar el servidor o cambiar el shared debemos abrir otra consola, ingresar al container

      > docker exec -it appserver bash

      Una vez ahi utilizamos vi (editor de texto) para modificar el archivo comandos.txt

      > vi comandos.txt

      .. warning:: Se recomienda antes de esto aprender a utilizar vi en el caso de no haber trabajado con el anteriormente.

      Una vez dentro de este archivo seguir los pasos mecionados en las secciones anteriores
      correspondientes a estas acciones.
