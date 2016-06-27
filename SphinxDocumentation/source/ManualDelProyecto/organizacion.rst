Organizacion del equipo de desarrollo
**************************************


Division de tareas
====================

  En esta seccion se mostrara a grandes rasgos la division de tareas que se realizo
  ademas de mostrar los cambios de personas entre modulos.

Primer Milestone
-----------------

Modulo cliente
+++++++++++++++

============================   ========================
Feature                         Asignados
============================   ========================
Registro                        Sebastian y Diego
Log in                          Sebastian y Diego
Pantalla principal              Sebastian y Diego
============================   ========================

.. note:: Se habia pensado hacer un chat basico tambien pero no pudo ser implementado


Modulo Application Server
+++++++++++++++++++++++++

============================   ========================
Feature                         Asignados
============================   ========================
Registro                        Juan Manual y Joaquin
Login                           Juan Manual y Joaquin
============================   ========================

.. note:: Se habia pensado hacer un chat basico tambien pero no pudo ser implementado


Modulo Shared Server
+++++++++++++++++++++++++

============================   ========================
Feature                         Asignados
============================   ========================
Registro                        Diego y Joaquin
Login                           Juan Manual y Joaquin
============================   ========================

Observaciones para el primer milestone
++++++++++++++++++++++++++++++++++++++++++++

No tratamos de entregar demasiadas funcionalidades para esta entrega ya que
consideramos el tiempo que nos llevaria aprender a utilizar todas las tecnologias
propuestas.

Nos dimos cuenta luego que tal vez con una persona el cliente podia ser desarrollado
y sumandole a esto los problemas que se nos presentaron tratando de trabajar en
conjunto utilizando un repositorio, decidimos asignarle el desarrollo del cliente
a Sebastian. A modo de prueba, pudiendo asignar mas personas si fuese necesario.






Segundo Milestone
-----------------


Modulo cliente
+++++++++++++++

============================   ========================
Feature / refactor                  Asignados
============================   ========================
Servicio de chat                     Sebastian
Administracion de imagenes           Sebastian
Servicio de match                    Sebastian
Refactorizaciones                    Sebastian
============================   ========================




Modulo Application Server
+++++++++++++++++++++++++

===================================   ==================================
Feature                                  Asignados
===================================   ==================================
Servicio de chat                       Juan Manual y Joaquin o Diego
Administracion de imagenes             Juan Manual y Joaquin o Diego
Almacenamiento de conversaciones       Juan Manual y Joaquin o Diego
Pruebas unitarias CPPUnit              Juan Manual y Joaquin o Diego
Integracion continua TRAVIS            Juan Manual y Joaquin o Diego
Virtualizacion con Docker              Juan Manual y Joaquin o Diego
Refactorizaciones                      Juan Manuel
===================================   ==================================



Modulo Shared Server
+++++++++++++++++++++++++

============================   ====================
Feature                         Asignados
============================   ====================
Cliente de bootstrap            Diego o Joaquin
Administracion de intereses     Diego o Joaquin
Administracion de imagenes      Diego o Joaquin
Virtualizacion (Docker)         Diego o Joaquin
============================   ====================


Observaciones para el segundo milestone
+++++++++++++++++++++++++++++++++++++++

En este milestone nos encontramos con bastantes problemas de organizacion
y comunicacion, uno de los peores fue hacer dos veces lo mismo para el shared
server.




Tercer milestone
-----------------

Modulo cliente
+++++++++++++++

=================================    ================
Feature / refactor                   Asignados
=================================    ================
Servicio de localizacion               Sebastian
Correcciones servicio de imagenes      Sebastian
Correcciones Servicio de match         Sebastian
Refactorizaciones                      Sebastian
=================================    ===============




Modulo Application Server
+++++++++++++++++++++++++

=======================================   ===========================
Feature                                             Asignados
=======================================   ===========================
Servicio de match                                   Juan Manual
Servicio de localizacion                            Juan Manual
Pruebas unitarias Google Test                 Juan Manual y Diego
Pruebas unitarias Google Mock                       Diego
Coverage                                        Diego y Juan Manuel
Virtualizacion con Docker                           Diego
Refactorizaciones                                 Juan Manuel
=======================================   ===========================



Modulo Shared Server
+++++++++++++++++++++++++

============================   =============
Feature                         Asignados
============================   =============
Cliente de bootstrap            Joaquin
Administracion de intereses     Joaquin
Administracion de imagenes      Joaquin
Virtualizacion (Docker)         Diego
============================   =============



Observaciones para el tercer milestone
+++++++++++++++++++++++++++++++++++++++

Nos jugo en contra el hecho de habernos organizado bien luego de tanto tiempo
ya a esta altura algunas personas que habian aprendido algunas tecnologias las
dejaron de lado para ponerse con otras y esto ademas de generar una sensacion
negativa provoco un defasaje entre los conocimientos tecnicos entre aquellos que
estuvieron firmes con una tecnologia en particular desde un principio y aquellos
que recien ahora habian definido bien sus roles.



Tracking de tickets
====================

**Changelog primer Milestone**
-----------------------------

Application Server
++++++++++++++++++++++++++++++++++

  Application Server:
  Change Log
  `[Unreleased] <https://github.com/seguijoaquin/taller2-appserver/tree/HEAD>`_

  **Implemented enhancements:**

  - Modificar el código para que utilize StringUtil `#13 <https://github.com/seguijoaquin/taller2-appserver/issues/13>`_
  - Sincronizar el servicio de registro con el alta en el shared `#11 <https://github.com/seguijoaquin/taller2-appserver/issues/11>`_

  **Fixed bugs:**

  - Sincronizar el servicio de registro con el alta en el shared `#11 <https://github.com/seguijoaquin/taller2-appserver/issues/11>`_
  - Arreglar el cmake para que se pueda usar el multithreading en el server `#10 <https://github.com/seguijoaquin/taller2-appserver/issues/10>`_

  **Closed issues:**

  - PRUEBAS: \[Error: The server does not support SSL connections\] `#9 <https://github.com/seguijoaquin/taller2-appserver/issues/9>`_
  - Integrar Rocksdb `#1 <https://github.com/seguijoaquin/taller2-appserver/issues/1>`_


Shared Server
+++++++++++++++++++++++++++++

  `Click aqui para ver el Changelog del Shared Server <https://github.com/seguijoaquin/taller2-sharedserver/blob/Checkpoint_1/CHANGELOG.md>`_

Cliente
+++++++++++++++++++++++++

  `Click aqui para ver el Changelog  del Cliente <https://github.com/diegofk26/taller2-cliente/blob/Checpoint_1/CHANGELOG.md>`_





**Changelog del Segundo milestone**
------------------------------------------


Application Server
++++++++++++++++++++++++++++++++++

  `Click aqui para ver el Changelog del Application Server <https://github.com/seguijoaquin/taller2-appserver/blob/Checkpoint_2/CHANGELOG.md>`_

Shared Server
+++++++++++++++++++++++++++++

  `Click aqui para ver el Changelog del Shared Server <https://github.com/seguijoaquin/taller2-sharedserver/blob/Checkpoint_2/CHANGELOG.md>`_

Cliente
+++++++++++++++++++++++++

  `Click aqui para ver el Changelog  del Cliente <https://github.com/diegofk26/taller2-cliente/blob/Checkpoint_2/CHANGELOG.md>`_




**Changelog del Tercer milestone**
----------------------------------

Application Server
++++++++++++++++++++++++++++++++++

  `Click aqui para ver el Changelog del Application Server <https://github.com/seguijoaquin/taller2-appserver/blob/Checkpoint_3/CHANGELOG.md>`_

Shared Server
+++++++++++++++++++++++++++++

  `Click aqui para ver el Changelog del Shared Server <https://github.com/seguijoaquin/taller2-sharedserver/blob/Checkpoint_3/CHANGELOG.md>`_

Cliente
+++++++++++++++++++++++++

  `Click aqui para ver el Changelog  del Cliente <https://github.com/diegofk26/taller2-cliente/blob/Checkpoint_3/CHANGELOG.md>`_
