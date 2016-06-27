Application Server - Taller de programación II  [Grupo 8]
********************************************************


Descripción
=======================

Se trata de una aplicación linux por consola destinada a mantenerse en ejecución por períodos prolongados de tiempo. Brinda una interfaz para la comunicación de los diferentes clientes que se conecten a la misma.

La interfaz de comunicación se realiza a traves de una Restful API, que define la forma de las solicitudes y respuestas de los diferentes servicios que brindará el servidor. Estos ultimos son:

Servicio de autenticación
----------------

El servidor dispondrá de un servicio para la autenticación de los clientes. Este servicio consta de una solicitud de autenticación, que viene junto con las credenciales del usuario. La respuesta a la solicitud es un token (identificador) de la sesión del usuario.

Servicio de búsqueda de candidato
----------------

El servidor provee un servicio en donde el usuario podrá solicitar un posible candidato para match.

Servicio de conversaciones
----------------


El servidor brindará un servicio para el delivery de conversaciones.

Para poder iniciar una conversación entre dos usuarios es necesario que exista un match entre ellos.



Contenidos
==========

.. toctree::
   :maxdepth: 3

   guiaInstalacion
   manualUsuario
   pruebas
